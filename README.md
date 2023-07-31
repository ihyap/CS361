# CS361 Microservice Project
A microservice for CS361 that receives user html form answers and returns a game recommendation statement.

## Requesting data

You can use the demo client included in this release as is or you can use it as a template to incorporate in to your own webpage. To request data, a python dictionary object must be written on request.json. The dictionary must have 5 entries with "play", "traitor", "duration", "complexity", and "interaction" as required keys. All keys and values pairs must be string.

```python
{"play": "Competitive Games", "traitor": "Non-Hidden Traitor", "duration": "Long Gameplay",
"complexity": "Simple", "interaction": "Little Interaction with Other Players"}
```


## Receiving data

Once you've requested data, the service will return a JSON string in request.json.

```python
"Oh! You might enjoy Simple Competitive Games with a Non-Hidden Traitor mechanic.
Look for something with Little Interaction with Other Players and a Long Gameplay."
```
The client webpage would simply need to read and process the JSON string.

```python
with open(json_file, "r") as f:
    message = json.load(f)
return message
```


## UML Sequence Diagram
<img src="https://github.com/ihyap/CS361/blob/main/uml%20diagram.jpg">
