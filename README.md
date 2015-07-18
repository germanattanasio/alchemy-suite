# Alchemy Suite

  The AlchemyAPI cloud platform makes it easy to create smart apps that deeply understand the world's conversations, reports and photos so you can align your business with customer preferences and intent. This Nodejs applications is running in [IBM Bluemix](https://bluemix.net) and shows all the alchemy services and allow you to type an input and see the output.
  
Give it a try! Click the button below to fork into IBM DevOps Services and deploy your own copy of this application on Bluemix.

[![Deploy to Bluemix](https://bluemix.net/deploy/button.png)](https://bluemix.net/deploy)

## Getting Started

1. Create a Bluemix Account

  [Sign up][sign_up] in Bluemix, or use an existing account. Watson Services in Beta are free to use.

2. Download and install the [Cloud-foundry CLI][cloud_foundry] tool

3. Edit the `manifest.yml` file and change the `<application-name>` to something unique.
  ```none
applications:
  name: <application-name>
  command: node app.js
  path: .
  memory: 256M
  ```
  The name you use will determinate your application url initially, e.g. `<application-name>.mybluemix.net`.

4. Connect to Bluemix in the command line tool
  ```sh
  $ cf api https://api.ng.bluemix.net
  $ cf login -u <your user ID>
  ```

5. Push it live!

  ```sh
  $ cf push
  ```

5. ADD the alchemy key(create one [here](http://www.alchemyapi.com/api/register.html)) to your environment

  ```sh
  $ cf se <application-name> ALCHEMY_KEY <alchemy-key>
  ```

## Running locally
  The application uses [Node.js](http://nodejs.org/) and [npm](https://www.npmjs.com/) so you will have to download and install them as part of the steps below.

1. Install [Node.js](http://nodejs.org/)
2. Go to the project folder in a terminal and run:
    `npm install`
3. Replace the `<alchemy-api>` placeholder
4. Start the application
   `node app.js`
5. Go to `http://localhost:3000`

## Troubleshooting

To troubleshoot your Bluemix app the main useful source of information are the logs, to see them, run:

  ```sh
  $ cf logs <application-name> --recent
  ```

## License

  This sample code is licensed under Apache 2.0. Full license text is available in [LICENSE](LICENSE).  
  This sample code uses bootstrap and jQuery, both distributed under MIT license.

## Contributing

  See [CONTRIBUTING](CONTRIBUTING.md).

## Open Source @ IBM
  Find more open source projects on the [IBM Github Page](http://ibm.github.io/)


[cloud_foundry]: https://github.com/cloudfoundry/cli
[sign_up]: https://apps.admin.ibmcloud.com/manage/trial/bluemix.html?cm_mmc=WatsonDeveloperCloud-_-LandingSiteGetStarted-_-x-_-CreateAnAccountOnBluemixCLI
