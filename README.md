# pause-on-succotash

Author: @ernestkoe, ernest.koe@proofgroup.com

`pause-on-succotash` is a bunch of javascript backend and frontend code to integrate Eventbrite, our event management app and Wix, the web site software platform for PauseOnError's. I wrote this for PoE St. Louis, 2020 and it's hardcoded to that event id; but pointing to a different event is fairly trivial.

## Installation

Ha. Installaion is just copy-pasta, sadly. Aslo, note that this was built with ES6 features that work on Wix but not necessarily with nodejs out of the box. I haven't gotten around to making this a generic app, yet.

## Usage

You'll need to configure an .env file with the following variables:

> API_AUTH=Bearer = YOURTOKENHERE
> API_URL=<https://www.eventbriteapi.com/v3/events/{YOUR-EVENT-ID-HERE}/attendees/>

The backend module code can be found in the `'backend` folder. Wix's names it's files with a `.jsw` extension, so you'll have to change that accordingly. `eventbriteUtils.js` contains the bits that recursively fetches data from eventbrite. `bModule.js` is a just a simple, single fetch call example.

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)
