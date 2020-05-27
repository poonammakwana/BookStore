# BookStore
netEnt/BookStore

This is an Book Store Application in Spring Boot Maven Build Tool. Database used H2Database.
Spring boot Rest APIs:


1. Add a book

curl --location --request POST 'http://localhost:8080/add' \
--header 'Content-Type: application/json' \
--data-raw '{
	"id" : 1,
	"isbn" : "Book2",
	"title" : "sunt aut facere repellat provident occaecati excepturi optio reprehenderit",
	"author" : "Poonam Makwana",
	"price" : 100.00,
	"copies" : 10
}'


2. Search a book by its ISBN or title or author

curl --location --request POST 'http://localhost:8080/search' \
--header 'Content-Type: application/json' \
--data-raw '{
	"isbn" : "Book1",
	"author" : "Poonam Makwana"
}'


3. Get the media Coverage by isbn

curl --location --request GET 'http://localhost:8080/mediaCoverage?isbn=Book1' \
--header 'Content-Type: application/json' \
--data-raw ''


4. Buy a book

curl --location --request GET 'http://localhost:8080/buyBook?isbn=Book1' \
--header 'Content-Type: application/json' \
--data-raw ''
