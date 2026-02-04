# ocp-webhook-receiver

oc -n openshift-monitoring edit configmap cluster-monitoring-config
```bash
apiVersion: v1
data:
  config.yaml: |
    enableUserWorkload: true
    alertmanagerMain:
      enableUserAlertmanagerConfig: true
```

oc -n openshift-user-workload-monitoring edit configmap user-workload-monitoring-config
```bash
apiVersion: v1
data:
  config.yaml: |
    alertmanager:
      enableAlertmanagerConfig: true
      enabled: true
```
