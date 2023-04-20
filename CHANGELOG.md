# 0.1.8

* Update Rasa container image to [the latest supported ver](https://github.com/opsdroid/opsdroid/pull/1963)
* Update Rasa deployment to the latest K8s version (tested on v1.26.3+k3s1)
* Add websocket connection to the default (example) config to avoid Opsdroid to fail on the start with the default configuration
* Make config mount in Opsdroid container read only