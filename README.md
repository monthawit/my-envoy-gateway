helm install eg oci://docker.io/envoyproxy/gateway-helm --version v1.6.0 -n envoy-gateway-system --create-namespace


helm upgrade --install eg oci://docker.io/envoyproxy/gateway-helm --version v1.6.0 -n envoy-gateway-system -f values.yaml


######### install monitor ###########


helm install eg-addons oci://docker.io/envoyproxy/gateway-addons-helm --version v1.6.0 --set opentelemetry-collector.enabled=true -n envoy-monitoring
