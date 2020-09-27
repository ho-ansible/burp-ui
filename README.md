# Ansible role: burp-ui
ziirish's web interface to Graham Keeling's `burp` backup software

## Requirements
Only tested on Debian stable, for now.

Assumes burp server and nginx are on same host.

## Role Variables
+ `burpui_host`: virtual host nginx listens for
+ `burpui_localport`: port on localhost that flask listens on
  (nginx will proxy to this port)
+ `burpui_listen`: array of nginx config 
  [`listen`](http://nginx.org/en/docs/http/ngx_http_core_module.html#listen) lines
+ `burpui_log`: flask logfile
+ Variables from the `burp` role are also used.

## Playbooks
+ `main.yml`: apply role
+ `uninstall.yml`: remove. Run before removing config from inventory.

## Dependencies
+ [ho-ansible.burp-server](https://github.com/ho-ansible/burp-server)
+ [ho-ansible.nginx](https://github.com/ho-ansible/nginx)

## License
+ burp-ui is licensed [BSD 3-clause](https://github.com/ziirish/burp-ui/blob/master/LICENSE).
+ This ansible role is licensed [MIT](LICENSE).

## Author Information
+ burp-ui is by [ziirish](https://github.com/ziirish/burp-ui)
+ This ansible role is by [Sean Ho](https://github.com/ho-ansible/)
