# fimi-Mock-Server

**Check out the [documentation of fimi](https://xu-chris.github.io/fimi-Documentation/) for full information about the whole system.**

fimi is an application which tries to resemble a coach while you doing workout by analyzing your posture and giving you feedback about what you should watch more often. To run it, you need a **webcam**, a big screen and your smartphone (and some room space). You control the big screen with your smartphone by simply scanning the displayed QR code (being in the same wifi net is necessary).

fimi generates a 3d pose estimation based on the webcam image and checks every frame your posture based on a fixed set of rules per exercise. In the end, you receive a small summary of your results on your smartphone.

The application also compares your posture with your previous trainings while still being designed with privacy in mind. All your information is stored only temporarily while running the application on your PC or Mac, whereas the training data is stored on your smartphone directly. This also means that you could theoretically log in at your friend's house and have your profile with you.

This is the mock server that simulates the [fimi Server](https://github.com/xu-chris/fimi-Server/) for rapid development of the [fimi Client](https://github.com/xu-chris/fimi-Client/). It sends repeatedly pose estimation data that were recorded previously with the [fimi Server](https://github.com/xu-chris/fimi-Server).

## Used technology
- [WebSockeetPP](https://github.com/zaphoyd/websocketpp)

## Build it
Create first the build folder with CMAKE or whatever tool you like. After that, build the project. Sicne it uses no other dependencies, you don't have to install any.

## Start it
Place your `test.mock` file into the `bin/Release/` folder and start `pose-estimator-server-mock` executable.

## Adjust it
You can change the following parameters:

- **`PORT_NUMBER`**: The port the WebSocket server is accepting connections and sending pose estimation data.

## How to create 
