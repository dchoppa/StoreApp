# WebStoreApp
Application for taking orders in a Queue

End point URLS:

An endpoint for adding items to the	queue. This endpoint takes only two parameters, the ID of the client and quantity

URI: http://localhost:8080/webstore/webapi/orders
Request type :PUT
Headers: Content-Type:application/json
Body:
{
        "client_id": "2000",
        "quantity": "10"
 }
 
 Post the orders one by one with above body.
 
  An endpoint for the client where he can check his queue position and approcimate wait time. Please give the Client_id at the path         parameter
  http://localhost:8080/webstore/webapi/orders/{200}
  
  An endpoint which allows Joe's manager to see all entries in the queue whic are about to deliver with the approximate wait time
  http://localhost:8080/webstore/webapi/orders/manager
  
  An endpoint to retrieve Joe next delivery which should be placed in the cart
  http://localhost:8080/webstore/webapi/orders/queue
  
  An endpoint to cancel an order. This endpoint should only the client ID. Please give the Client_id at the path parameter
  http://localhost:8080/webstore/webapi/orders/{2000}
  
  
  Note: There is no database configured and all the orders memory is stored in a Static Queue. Please use any convenient Restclient for different types of requests.
  
  
  
  
