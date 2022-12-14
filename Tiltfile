def create_namespace(name):
    k8s_yaml(blob("""apiVersion: v1
kind: Namespace
metadata:
  name: %s
""" % name))

name = "percona-pmm-test"

create_namespace(name)

k8s_yaml(helm("charts/pmm", name, namespace = name))
