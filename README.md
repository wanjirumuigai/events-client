
# Events Board

This project manages the events at ARC College. It shows the upcoming events, the venue of the event and staff assigned to that event. User can create an event, assign staff to an event, update other event details and delete an event.

# API

# Endpoints

http://localhost:9292/events
This endpoint shows the list of all events
[
{"id":3,"name":"SNE Conference","event_type":"Internal","number_of_participants":350,"status":"confirmed","event_date":"2023-04-29T00:00:00.000Z","venue_id":1,"event_staff_id":null,
"venue":
    {"id":1,
    "name":"Dias",
    "capacity":500}
},

{"id":6,"name":"HoDs meeting","event_type":"Internal","number_of_participants":20,"status":"confirmed","event_date":"2023-05-02T00:00:00.000Z","venue_id":3,"event_staff_id":10,
"venue":
    {"id":3,
    "name":"Simba",
    "capacity":20}
},

{"id":7,"name":"Funkids Entertainment","event_type":"Internal","number_of_participants":500,"status":"confirmed","event_date":"2023-05-16T00:00:00.000Z","venue_id":1,"event_staff_id":11,
"venue":
    {"id":1,
    "name":"Dias",
    "capacity":500}
},]

http://localhost:9292/venues
This endpoint shows a list of all venues 
[
{"id":1,"name":"Dias","capacity":500},
{"id":2,"name":"Kifaru","capacity":15},
{"id":3,"name":"Simba","capacity":20},
{"id":4,"name":"Seneiya","capacity":100}
]
http://localhost:9292//events/:id
This endpoint shows details of a particular event


    {
        "id":4,
        "name":"Graduation",
        "event_type":"Internal",
        "number_of_participants":500,
        "status":"pending",
        "event_date":"2023-06-03T00:00:00.000Z",
        "venue_id":1,
        "event_staff_id":6
    }


# Routes
get "/events" 

This route fetches all the events
  
  get "/events/:id" 
This route fetches an event by id

 
get "/event_staff/:id" do
This route fetches the staff assigned to an event

get "/venues" do
This route fetches all the venues

  get "/staff" do
 This route fetches all the staff


  patch "/events_staffs/:id" do
  This route updates the staff assigned to an event

  patch "/events/:id" do
 This route updates an event

  post "/events" do
  This route creates a new event

  delete "/events/:id" do
This route deletes an event