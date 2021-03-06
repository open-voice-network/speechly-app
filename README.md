# Speechly App

This is a React component that demonstrates [Speechly](https://www.npmjs.com/package/@speechly/react-client) 
interoperability with [Genie](https://wiki.almond.stanford.edu/api-references/web-almond) and Magenta smart assistants.

_Note that you will need to have [Node.js](https://nodejs.org) (tested on v16.14.2) installed._

## Get started

```bash
git clone https://github.com/open-voice-network/speechly-app.git
cd speechly-app
npm install
```

> **Note**: for simplicity, we skip authentication part and assume you have a valid access token. 

Add `App ID` and auth token to `./.env`:

```env
# Genie settings
REACT_APP_ACCESS_TOKEN="your-access-token"
REACT_APP_APP_ID="your-app-id"

# Magenta settings
REACT_APP_BASE_URL="magenta-server-url"
REACT_APP_API_KEY="magenta-api-key"
EACT_APP_TESTING_SECRET="magenta-testing-secret"

# Google API key for translation
REACT_APP_GOOGLE_API_KEY="your-google-api-key"
```

Start the development server

```bash
npm start
```

Navigate to [localhost:3000](http://localhost:3000) and you should see your app running. 
Open the Developer Console to see speech segments and raw responses from Genie/Magenta.


## Usage

Click and hold Push-to-Talk button at the bottom of the screen.

To ask a single question from Magenta: _**"Ask Magenta <question>"**_, e.g: **_"ask Magenta the weather in London"_**

To ask a single question from Genie: _**"Ask Genie <question>"**_, e.g: **_"ask Genie a joke"_**

To activate Magenta: **_"Launch Magenta"_**. After the launch, all user queries will be sent to Magenta Platform.
To stop Magenta: **_"Stop Magenta"_**.


To connect to Genie cloud : **_"Launch Genie"_**. To terminate connection: **_"Stop Genie"_**.
