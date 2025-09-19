# 创建kibana账号
curl -u elastic:changeme -X POST http://localhost:9200/_security/user/kibana_service \
-H "Content-Type: application/json" \
-d '{
"password" : "MyKibana@2025",
"roles" : [ "kibana_system" ],
"full_name" : "Kibana service user",
"email" : "kibana@example.com"
}'