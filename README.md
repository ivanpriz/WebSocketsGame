Online game with movement mechanic. 

You can move from cell to cell and can not collide with other players.

Consist of:
1) HTML & JS client
2) Commands service - FastAPI websockets server. Processes user input and sends commands to other services.
3) Render service - python service. Get tasks to render game board from commands service and returns rendered boards for it to send to users. Also produces logs to commands service. The communication is done via RabbitMQ.
4) Users service - stores users info. Currently it is username and color. Communicates with other services via RabbitMQ.

Setting up locally with docker-compose:
1) `docker-compose build`
2) `docker-compose up -d`


Game is available on port 5252!
