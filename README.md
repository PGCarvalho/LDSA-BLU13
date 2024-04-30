App to be deployed with Railway

STEPS:
New project
Add new service -> github repo -> pick this one
Add new service -> database -> postgreSQL
Add 2 new variables to server
 -> PORT - 5000
 -> DATABASE_URL <default value>
Deploy
Settings -> netwrking -> create url


Do not forget to delete all services when done using
-

Example commands to run:
curl -X POST https://ldsa-blu13-production.up.railway.app/predict -d '{"id": 0, "observation": {"age": 45, "education": "Bachelors", "hours-per-week": 45, "native-country": "United-States"}}' -H "Content-Type:application/json"

curl -X POST https://ldsa-blu13-production.up.railway.app/predict -d '{"id": 0, "observation": {"age": 45, "education": "Bachelors", "hours-per-week": 45, "native-country": "United-States"}}' -H "Content-Type:application/json"

curl -X POST https://ldsa-blu13-production.up.railway.app/predict -d '{"id": 1, "observation": {"age": 45, "education": "Bachelors", "hours-per-week": "45 hours", "native-country": "United-States"}}' -H "Content-Type:application/json"

curl -X POST https://ldsa-blu13-production.up.railway.app/update -d '{"id": 0, "true_class": 1}'  -H "Content-Type:application/json"

curl -X POST https://ldsa-blu13-production.up.railway.app/update -d '{"id": 3, "true_class": 1}'  -H "Content-Type:application/json"
