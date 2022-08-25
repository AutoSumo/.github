AutoSumo is a project enabling remote programming of a robot that accomplishes tasks in an automatically tracked arena.
Originally developed for sumo robotics, the robot platform is designed to be extensible.

The [robot](https://github.com/AutoSumo/robot) itself was designed from scratch and 3D-printed.

## Media

https://user-images.githubusercontent.com/26680599/185769401-c024f6a5-496c-4001-9858-a5e7ccef9a41.mp4

![Robot body in Fusion 360](https://user-images.githubusercontent.com/26680599/186747566-b6fe78d5-234d-42a8-a620-afc675234ee1.png)
![Picture of the robot](https://user-images.githubusercontent.com/26680599/186748286-b1a7dc94-7e34-44f7-9d12-4bc15a54bf48.jpg)
![Picture of the underside of the robot](https://user-images.githubusercontent.com/26680599/186748291-354b9bca-f11a-4f92-94e0-9022a0ad5487.jpg)

## Project Structure

```mermaid
flowchart TD
    web["🌐 Web Interface"] -->|uploads code| code-server[("💾 Code Server")]
    code-server -->|highlight data| web
    code-server -->|downloads code| bot-server["💻 Bot Server"]
    bot-server -->|highlight data| code-server
    bot-server -->|motor instructions| robot["🤖 Robot"]
    robot -->|sensor data| bot-server
    tag-server["📷 Tag Server"] -->|apriltag positions| bot-server
        
    click web "https://github.com/AutoSumo/web"
    click code-server "https://github.com/AutoSumo/code-server"
    click bot-server "https://github.com/AutoSumo/server"
    click tag-server "https://github.com/AutoSumo/tag-server"
    click robot "https://github.com/AutoSumo/robot"
```
