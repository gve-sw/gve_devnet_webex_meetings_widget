# Webex React Meeting Widget Sample

This sample code shows the use of the [Webex Meetings Widget](https://developer.webex.com/docs/widgets#meetings-widget-) in a simple React App. The instructions cover how to build the app and how to embed it as a component in static or dynamic template HTML pages. 

   > This sample code was created based on the [Webex React Meeting Widget Starter](https://github.com/WebexSamples/webex-meeting-widget-starter) repository.


## Contacts
* ramrenne

## Installation

1. Make sure you have the following tools installed: 
  * [Node.js v14.19.0](https://nodejs.org/en/blog/release/v14.19.0/) (including npm)
  * [Yarn v1.22.17](https://classic.yarnpkg.com/lang/en/docs/install)
  * [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)


2. Clone this Github repository into a local folder:  
  ```git clone [add github link here]```
  * For Github link: 
      In Github, click on the **Clone or download** button in the upper part of the page > click the **copy icon**  
      ![/IMAGES/giturl.png](/IMAGES/giturl.png)
  * Or simply download the repository as zip file using 'Download ZIP' button and extract it

3. Access the downloaded folder:  
    ```cd gve_devnet_webex_meetings_widget```

4. Install the dependencies via:   
  ``` yarn install ```

5. Create a [Personal Access Token](https://developer.webex.com/docs/getting-started) or [Guest Token](https://developer.webex.com/docs/guest-issuer) for the next step. 
   > Personal Access Tokens have only a short lifetime (12 hours) and are meant for testing purposes. An alternative are tokens retrieved via the oAuth workflow. The [Webex React Meeting Widget Starter](https://github.com/WebexSamples/webex-meeting-widget-starter) shows an integration of the Webex Meetings Widget and oAuth.

6. Fill in your variables in the **index.html** file:      
      
  ```  
    ...
    <div id="meetings-widget" 
    data-token="[Personal Access or Guest Token token from 5]" 
    data-destination="[Destination]">
    </div>
    ....
  ```

  > A meeting destination is a virtual location where the Webex meeting takes place. It can be: SIP URI (Webex Meetings, Personal Meeting Rooms and Webex cloud-registered devices only), email address (of a Webex user), people ID, room ID.

7. Run the React application in development mode via:   
  ``` yarn start ```

Open [http://localhost:3000](http://localhost:3000) in the browser to view the app. 


## Embed the Widget as a Component in a Dynamic Template or Static HTML Page

## Build application for production

1. Build the application for production:   
   ``` yarn build:widget ```

2. The build creates several files in a new folder - **gve_devnet_webex_meetings_widget/dist**. We will use these files in the next step.

## Embed the Component in the Target HTML page

In target HTML page:

1. Embed the Widget by copying the following files into the preferred directories:

* index.css
* index.js
* several .woff, .woff2, .svg (keep these in same folder as index.css or adapt the reference in the index.css)

2. Add the references to the mentioned files and a div tag with **id="meetings-widget"** as shown in the following sample:

 ```  

  <!doctype html>
    <html lang="en">

      <head>

        <link rel="stylesheet" href="static/css/index.css"> 

      </head>

      <body>

        <div id="meetings-widget" 
            data-token="[Add api token]" 
            data-destination="[Add destination]"></div>

        <script src='static/js/index.js'></script>

      </body>
    </html>  

  ```


3. Fill in the API token and destination as value for the **data-token** and **data-destination** attribute

4. Open the website in a browser to view the embedded widget

   > Note: Please be aware that a website has to use https for the embedded widget to work correctly.


## Screenshots

![/IMAGES/before_call.png](/IMAGES/before_call.png)
![/IMAGES/call_no_participants_tab.png](/IMAGES/call_no_participants_tab.png)
![/IMAGES/call_participants.png](/IMAGES/call_participants.png)


## Further Useful Resources

 - [Webex Widgets](https://developer.webex.com/docs/widgets)
 - Webex Widgets Github: [Link 1](https://github.com/webex/widgets#webex-widgets) [Link 2](https://github.com/webex/widgets/tree/master/src/widgets/WebexMeetings#webex-meetings-widget)
 - [Webex React Meeting Widget Starter](https://github.com/WebexSamples/webex-meeting-widget-starter)
 - [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started)
 - [React documentation](https://reactjs.org/)


### LICENSE

Provided under Cisco Sample Code License, for details see [LICENSE](LICENSE.md)

### CODE_OF_CONDUCT

Our code of conduct is available [here](CODE_OF_CONDUCT.md)

### CONTRIBUTING

See our contributing guidelines [here](CONTRIBUTING.md)

#### DISCLAIMER:
<b>Please note:</b> This script is meant for demo purposes only. All tools/ scripts in this repo are released for use "AS IS" without any warranties of any kind, including, but not limited to their installation, use, or performance. Any use of these scripts and tools is at your own risk. There is no guarantee that they have been through thorough testing in a comparable environment and we are not responsible for any damage or data loss incurred with their use.
You are responsible for reviewing and testing any scripts you run thoroughly before use in any non-testing environment.