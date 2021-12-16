---
layout: default
---
# Project
OpenVVC is open-source real time software decoder compliant with the ITU-T H.266- MPEG-I - Part 3 VVC standard. OpenVVC is developed from scratch in C as a library that provides consumers with real time and energy-aware decoding capabilities under different OS including MAC OS, Windows, Linux and Android targeting low energy real-time decoding of 4K VVC videos on Intel x86 and ARM platforms.

# Supported tools
<table id="toolTable">
<colgroup>
<col width="15%" />
<col width="30%" />
<col width="10%" />
<col width="10%" />
<col width="10%" />
</colgroup>
<thead>
  <tr>
    <th>VVC Tools Category</th>
    <th>VVC Tools</th>
    <th style="text-align: center;">Full support</th>
    <th style="text-align: center;">x86 SIMD</th>
    <th style="text-align: center;">ARM SIMD</th>
  </tr>
</thead>
  <tbody>
    {% for tool in site.data.supported_tools %}
      <tr>
        {% if tool.rowspan != null and tool.rowspan != "" %}
          <td rowspan={{tool.rowspan}}>{{tool.VVC_Tools_category}}</td>
        {% endif %}
        <td >{{tool.VVC_Tools}}</td>
        {% case tool.Template %}
          {% when "1" %}
            <td class="toolok"></td>
          {% when "2" %}
            <td class="tooloknok"></td>
          {% when "3" %}
            <td class="toolnok"></td>
          {% else %}
            <td class="toolna"></td>
        {% endcase %}
        {% if tool.SSE2 == "1" or tool.SSE4 == "1" or tool.AVX2 == "1" %}
          <td class="toolok"></td>
        {% elsif tool.SSE2 == "2" or tool.SSE4 == "2" or tool.AVX2 == "2" %}
          <td class="tooloknok"></td>
        {% elsif tool.SSE2 == "3" or tool.SSE4 == "3" or tool.AVX2 == "3" or tool.SSE2 == "4" or tool.SSE4 == "4" or tool.AVX2 == "4" %}
          <td class="toolnok"></td>
        {% else %}
          <td class="toolna"></td>
        {% endif %}
        {% case tool.NEON %}
          {% when "1" %}
            <td class="toolok"></td>
          {% when "2" %}
            <td class="tooloknok"></td>
          {% when "3" or "4" %}
            <td class="toolnok"></td>
          {% else %}
            <td class="toolna"></td>
        {% endcase %}
      </tr>
    {% endfor %}
  </tbody>
</table>

# Contributors

  - Pierre-Loup Cabarat
  - Wassim Hamidouche
  - Thomas Amestoy
  - Guillaume Gautier

# Acknowledgements

<span class="logo_container"><img class="logo-ack" src="./assets/images/Logo_INSA.png"/></span>
<span class="logo_container"><img class="logo-ack" src="./assets/images/Logo_IETR.png"/></span>
<span class="logo_container" style="width: 12%;"><img class="logo-ack" src="./assets/images/Logo_RB.jpg"/></span>
<span class="logo_container"><img class="logo-ack" src="./assets/images/Logo_SATT.png"/></span>
