Web Sockets
    -Communication protocol to transmit data between computers
Real time features
    -Monitor when someone is typing
    -Messaging apps
    -See if someone is online or not
    -real time data

Fast, Lightweight, Supported by the browser
-The connection is persistent and maintained unlike in http where the connection ends as soon as the serever sends a http response
-No need to re establish connection and fo through authentication process

Patterns of Ws
-Pub Sub
    -Only sends data in one wa y
    -one publisher(server)
    -A lot of subscribers(clients)
    -E.g financial app, streaming live financial data
        -Video streaming platforms
        -CCTV 

-RPC
    -Two way communication protocol
    -remote function calls(server returns response from functions)
    -Only happens with one client
    -Used in chat messaging

Mesaging uses both pubSub and RPC for one to one and one to many chats

Laravel Has inbuilt suport for pub sub
-configure web socket server in laravel
-Pusher, ably - web socket server - subscriptions
-Laravel websockets

