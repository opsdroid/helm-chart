<html>
<body>

<p>See installation instructions at:</p>

<ul>
<li><a href="https://github.com/opsdroid/helm-chart">Opsdroid</a></li>
</ul>

<h2>Stable releases</h2>
{% assign opsdroid = site.data.index.entries.opsdroid | sort: 'created' | reverse %}
{% assign all_charts = opsdroid %}
<table>
  <tr>
    <th>chart version</th>
    <th>app version</th>
    <th>date</th>
  </tr>
  {% for chart in all_charts %}
    {% unless chart.version contains "-" %}
    <tr>
      <td>
      <a href="{{ chart.urls[0] }}">
          {{ chart.name }}-{{ chart.version }}
      </a>
      </td>
      <td>
          <a href="https://docs.opsdroid.dev/en/v{{ chart.appVersion }}/">
              {{ chart.appVersion }}
          </a>
      </td>
      <td>
          <span class='date'>{{ chart.created | date_to_rfc822 }}</span>
      </td>
    </tr>
    {% endunless %}
  {% endfor %}
</table>

</body>
</html>
