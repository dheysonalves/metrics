<!--header-->
<table>
  <tr><th colspan="2"><h3>📰 Recent activity</h3></th></tr>
  <tr><td colspan="2" align="center"><p>This plugin displays your recent activity on GitHub.</p>
</td></tr>
  <tr>
    <th rowspan="3">Supported features<br><sub><a href="metadata.yml">→ Full specification</a></sub></th>
    <td><a href="/source/templates/classic/README.md"><code>📗 Classic template</code></a> <a href="/source/templates/markdown/README.md"><code>📒 Markdown template</code></a> <a href="/source/templates/repository/README.md"><code>📘 Repository template</code></a></td>
  </tr>
  <tr>
    <td><code>👤 Users</code> <code>👥 Organizations</code> <code>📓 Repositories</code></td>
  </tr>
  <tr>
    <td><code>🔑 (scopeless)</code> <code>read:org (optional)</code> <code>read:user (optional)</code> <code>repo (optional)</code></td>
  </tr>
  <tr>
    <td colspan="2" align="center">
      <img src="https://github.com/lowlighter/metrics/blob/examples/metrics.plugin.activity.svg" alt=""></img>
      <img width="900" height="1" alt="">
    </td>
  </tr>
</table>
<!--/header-->

## ➡️ Available options

<!--options-->
<table>
  <tr>
    <td align="center" nowrap="nowrap">Type</i></td><td align="center" nowrap="nowrap">Description</td>
  </tr>
  <tr>
    <td nowrap="nowrap"><code>plugin_activity</code></td>
    <td rowspan="2"><p>Enable activity plugin</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>boolean</code>
<br>
<b>default:</b> no<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><code>plugin_activity_limit</code></td>
    <td rowspan="2"><p>Display limit</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>number</code>
<i>(1 ≤
𝑥
≤ 1000)</i>
<br>
<b>default:</b> 5<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><code>plugin_activity_load</code></td>
    <td rowspan="2"><p>Events to load</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>number</code>
<i>(100 ≤
𝑥
≤ 1000)</i>
<br>
<b>default:</b> 300<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><code>plugin_activity_days</code></td>
    <td rowspan="2"><p>Events maximum age</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>number</code>
<i>(0 ≤
𝑥
≤ 365)</i>
<br>
<b>zero behaviour:</b> disable</br>
<b>default:</b> 14<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><code>plugin_activity_visibility</code></td>
    <td rowspan="2"><p>Events visibility</p>
<p>Lets you hide private activity when using a <code>repo</code> scope token</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>string</code>
<br>
<b>default:</b> all<br>
<b>allowed values:</b><ul><li>public</li><li>all</li></ul></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><code>plugin_activity_timestamps</code></td>
    <td rowspan="2"><p>Display events timestamps</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>boolean</code>
<br>
<b>default:</b> no<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><code>plugin_activity_skipped</code></td>
    <td rowspan="2"><p>Skipped repositories</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap">⏩ Inherits <code>repositories_skipped</code><br>
<b>type:</b> <code>array</code>
<i>(comma-separated)</i>
<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><code>plugin_activity_ignored</code></td>
    <td rowspan="2"><p>Ignored users</p>
<p>Useful to ignore bots activity</p>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap">⏩ Inherits <code>users_ignored</code><br>
<b>type:</b> <code>array</code>
<i>(comma-separated)</i>
<br></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><code>plugin_activity_filter</code></td>
    <td rowspan="2"><p>Events types</p>
<p>These are fetched from <a href="https://docs.github.com/en/free-pro-team@latest/developers/webhooks-and-events/github-event-types">GitHub events API</a> and the following types are currently supported:</p>
<ul>
<li><code>push</code>: Push of commits</li>
<li><code>issue</code>: Opening/Reopening/Closing of issues</li>
<li><code>pr</code>: Opening/Closing of pull requests</li>
<li>`ref/create: Creation of git tags or git branches</li>
<li>`ref/delete: Deletion of git tags or git branches</li>
<li><code>release</code>: Publication of new releases</li>
<li><code>review</code>: Review of pull requests</li>
<li><code>comment</code>: Comments on commits, issues and pull requests</li>
<li><code>wiki</code>: Edition of wiki pages</li>
<li><code>fork</code>: Forking of repositories</li>
<li><code>star</code>: Starring of repositories</li>
<li><code>public</code>: Repositories made public</li>
<li><code>member</code>: Addition of new collaborator in repository</li>
</ul>
<img width="900" height="1" alt=""></td>
  </tr>
  <tr>
    <td nowrap="nowrap"><b>type:</b> <code>array</code>
<i>(comma-separated)</i>
<br>
<b>default:</b> all<br>
<b>allowed values:</b><ul><li>all</li><li>comment</li><li>ref/create</li><li>ref/delete</li><li>release</li><li>push</li><li>issue</li><li>pr</li><li>review</li><li>wiki</li><li>fork</li><li>star</li><li>member</li><li>public</li></ul></td>
  </tr>
</table>
<!--/options-->

## ℹ️ Examples workflows

<!--examples-->
```yaml
name: Recent activity
uses: lowlighter/metrics@latest
with:
  filename: metrics.plugin.activity.svg
  token: ${{ secrets.METRICS_TOKEN }}
  base: ""
  plugin_activity: yes
  plugin_activity_limit: 5
  plugin_activity_days: 0
  plugin_activity_filter: issue, pr, release, fork, review, ref/create

```
<!--/examples-->
