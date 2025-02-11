This is just an experimentation with function calling

Run with

~~~bash
podman-compose up
~~~

The python container should print out something like :

~~~
[python] | DEBUG - Executing tool call : function=Function(name='get_current_weather', arguments={'city': 'Toronto'})
[python] | DEBUG - Function returned with : It's sunny out here !
[python] | DEBUG - Executing tool call : function=Function(name='get_current_weather', arguments={'city': 'Paris'})
[python] | DEBUG - Function returned with : It's raining today
[python] | Based on the tool call responses, I can provide you with the following information:
[python] |
[python] | The weather in Toronto is sunny.
[python] |
[python] | The weather in Paris is rainy.
~~~

