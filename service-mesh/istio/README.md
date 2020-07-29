helm --namespace istio-system template install/kubernetes/helm/istio  \   
--set global.controlPlaneSecurityEnabled=true \   
--set mixer.adapters.useAdapterCRDs=true \   
--set grafana.enabled=true --set grafana.security.enabled=true \   
--set tracing.enabled=true \   
--set kiali.enabled=true \   
--set istio_cni.enabled=true \   
--set global.mtls.enabled=true \   
--set gateways.istio-ingressgateway.serviceAnnotations.'service\.beta\.kubernetes\.io/azure-load-balancer-internal'="true" \   
--set gateways.istio-egressgateway.enabled=false \   
--set certmanager.email=someone@example.com \   
--set certmanager.enabled=true \   
--set sidecarInjectorWebhook.rewriteAppHTTPProbe=true \|
 kubectl apply -f -