helm install elasticsearch elastic/elasticsearch -f ./values_elastick.yaml

helm install  kibana elastic/kibana

helm install logstash elastic/logstash -f ./values_logstash.yaml



check logstash paiplines
kubectl exec -tii logstash-logstash-0 bash
cat /usr/share/logstash/pipeline/logstash.conf


to get access to kibana
kubectl port-forward  kibana-kibana-84579f77bc-khz88 5601:5601











