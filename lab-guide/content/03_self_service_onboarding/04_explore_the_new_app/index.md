## Explore the New App

### Browse to the newly deployed app - SimpleNodeService

![Browse App](../../../assets/images/03_04_explore_new_app.png)

Once Argo has deployed our app we can access it from various locations
1. From the **Backstage** component page, locate and click on `Browse Application` to open the newly created application.
2. From **ArgoCD** you can click on the link in the top right corner of the App
3. In **Dynatrace** you can find the links in the Platform Observability Cockpit Dashboard. Select your application in the dashboard variable and find the deployment event and link in the bottom right table

**Explore the app**
The application is really simple. Most likely you have deployed version 1.0.2 of the app which has a green background color. In the slides you can see that versions 2.0.2, 3.0.2 and 4.0.2 have different colors. They also have different `built-in problems` which we can explore later on. In a later hands-on excercise we will deploy different versions!

Right now feel free to quickly explore the `limited` functionality of the app. Clicking on the `Echo` and `Invoke` buttons will generate activity and transactions on the new application.