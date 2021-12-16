---
layout: default
---

# Performance
## Graph Performance
## Choix
  - platforms( x86 / ARM)
  - optimisation
  - single/multi thread

## tableau
<table>
<!-- <colgroup>
<col width="15%" />
<col width="30%" />
<col width="10%" />
<col width="10%" />
<col width="10%" />
</colgroup> -->
<thead>
  <tr>
    <th rowspan="4">Class</th>
    <th rowspan="4">Sequence name</th>
    <th rowspan="4">Resolution</th>
    <!-- <th rowspan="4">Frame count</th> -->
    <!-- <th rowspan="4">Frame rate</th> -->
    <!-- <th rowspan="4">Bit depth</th> -->
    <th colspan="12">X86</th>
  </tr>
  <tr>
    <th colspan="4">AI</th>
    <th colspan="4">LD</th>
    <th colspan="4">RA</th>
  </tr>
  <tr>
    <th>QP 22</th>
    <th>QP 27</th>
    <th>QP 32</th>
    <th>QP 37</th>
    <th>QP 22</th>
    <th>QP 27</th>
    <th>QP 32</th>
    <th>QP 37</th>
    <th>QP 22</th>
    <th>QP 27</th>
    <th>QP 32</th>
    <th>QP 37</th>
  </tr>
</thead>
  <tbody>
    {% for sequence in site.data.X86perf %}
      <tr>
        {% if sequence.rowspan != null and sequence.rowspan != "" %}
          <td rowspan={{sequence.rowspan}}>{{sequence.Class}}</td>
        {% endif %}
        <td>{{sequence.name}}</td>
        <td>{{sequence.Resolution}}</td>
        <!-- <td>{{sequence.Frame_count}}</td> -->
        <!-- <td>{{sequence.Frame_rate}}</td> -->
        <!-- <td>{{sequence.Bit_depth}}</td> -->
      </tr>
    {% endfor %}
  </tbody>
</table>
<!-- # Citation
```

``` -->