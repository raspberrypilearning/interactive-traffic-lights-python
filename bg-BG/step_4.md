## Светофар

Можете да използвате вградената `TrafficLights` интерфейс вместо три светодиода.

1. Промяна на `от импортиране на gpiozero ...` линия за замяна `LED` с `TrafficLights`:
    
    ```python
от gpiozero импортиране на TrafficLights, бутон от бутона за време за внос на сън = бутон (25) светлини = TrafficLights (24, 23, 22), докато True: button.wait_for_press () lights.on
```

2. Опитайте да промените осветлението на `мига`:
    
    ```python
докато Истина: lights.blink () button.wait_for_press () lights.off () button.wait_for_release ()
```