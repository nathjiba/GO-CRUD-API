# Simple CRUD API in Go
run below command in the workspace
go get ./...

Below operations are exposed:-
[GIN-debug] GET    /people/                  --> main.GetPeople (3 handlers)
[GIN-debug] GET    /people/:id               --> main.GetPerson (3 handlers)
[GIN-debug] POST   /people                   --> main.CreatePerson (3 handlers)
[GIN-debug] PUT    /people/:id               --> main.UpdatePerson (3 handlers)
[GIN-debug] DELETE /people/:id               --> main.DeletePerson (3 handlers)



curl -X POST \
  http://localhost:8080/people \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -H 'postman-token: 3f6e1b4b-21df-5c5c-c34f-9758c96d427d' \
  -d '{"id":1,"firstname":"arya","lastname":"start","city":"north"}'


curl -X GET \
  http://localhost:8080/people


curl -X PUT \
  http://localhost:8080/people/1 \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -H 'postman-token: 4546140c-1053-4815-c35d-1dcf0ae55114' \
  -d '{"id":1,"firstname":"arya","lastname":"net stark","city":"north"}'

curl -X DELETE \
  http://localhost:8080/people/2