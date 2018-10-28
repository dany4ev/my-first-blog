Your API token
62540efcdafa59c9342926980cacc7a46e55be1e
Warning: our API is new and in beta and not officially supported, and may change at any time, and it is not to be relied upon, and may cause unpredictable growth of extra ears. Extra ears not guaranteed.

Use this token for our API by setting a request header called Authorization, followed by Token <token>, eg:

import requests
my_domain = 'dany4ev.pythonanywhere.com'
username = 'dany4ev'
token = '62540efcdafa59c9342926980cacc7a46e55be1e'

response = requests.post(
  'https://www.pythonanywhere.com/api/v0/user/{username}/webapps/{domain}/reload/'.format(
      username=username, domain=my_domain
  ),
  headers={'Authorization': 'Token {token}'.format(token=token)}
)
if response.status_code == 200:
  print('All OK')
else:
  print('Got unexpected status code {}: {!r}'.format(response.status_code, response.content))
                        
TIP: Your API token is also available from pythonanywhere consoles, tasks and webapps, as an Environment Variable, $API_TOKEN

API documentation
You can find the latest documentation in our help pages:

help.pythonanywhere.com/pages/API