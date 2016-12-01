Uptime Slack webhook plugin
===========================

This [Uptime](https://github.com/fzaninotto/uptime) plugin notifies all configured events (up, down, paused, restarted) by sending a HTTPS POST request to a slack.com URL.

Based on [mintbridge/uptime-webhooks](https://github.com/mintbridge/uptime-webhooks) plugin.

To use this plugin, first install it using npm while in the Uptime directory:

```sh
$ npm install uptime-slack
```

Then to enable it, add it to the `config/production.js`, as follows:

```js
...
plugins:
  ...
  - ./node_modules/uptime-slack
```

Customize the plugin settings in the `config/production.yaml` configuration file, as in the example below:

```yaml
webhooks:
  event:
    up:
      - 'https://hooks.slack.com/services/ABC/DEF/GHI'
    down:
      - 'https://hooks.slack.com/services/ABC/DEF/GHI'
    paused:
      - 'https://hooks.slack.com/services/ABC/DEF/GHI'
    restarted:
      - 'https://hooks.slack.com/services/ABC/DEF/GHI'
  dashboardUrl: 'http://uptime.example.com'
  channel:      '#slack-channel'
  username:     'uptime'
  icon_emoji:   ':fire:'
```
