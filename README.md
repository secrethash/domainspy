domainspy helps you monitor domains for availability. Provide a list of domains
that you care about, run the script, and domainspy will tell you if any of them
are available.

You might want to consider running domainspy automatically, for example as a
cron job, and having the results emailed to you.

domainspy uses the [namecheap.domains.check method](https://www.namecheap.com/support/api/methods/domains/check.aspx)
of the [Namecheap API](https://www.namecheap.com/support/api/intro.aspx).

## Usage

### Set up

1. Set up the API
    1. Sign up for a free [Namecheap API](https://www.namecheap.com/support/api/intro.aspx) account
        * If Namecheap doesn't respond to your request for API access within a
          couple of days, contact support. They can usually speed things up.
        * You don't need to request sandbox API access unless you plan to modify
          or test this script.
    2. Make note of your username and API key
    3. Whitelist your IP address in the Namecheap API settings
2. Create a file named *domains.json* at the root of this repository. The file
   should be an array of strings, where each string is a domain that you want to
   monitor. For example:

   ```json
   [
       "example.com",
       "google.com",
       "github.com"
   ]
   ```

### Install

1. [Install Node and NPM](https://nodejs.org/en/download/)
2. Run `npm install`

### Run

Run `USERNAME=username API_KEY=apikey CLIENT_IP=ipaddress npm start`

Tip: To set your IP address automatically, try something like this:
`` CLIENT_IP=`curl --silent icanhazip.com` ``

### Test

Run `npm test`
