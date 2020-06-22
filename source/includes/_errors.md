# Possible Errors

Sometimes, your API calls may encounter any of the following errors. In a perfect scenario, your code should expect and handle these errors.

Code | Details
---------- | -------
400 | Bad request. Our server didn't understand your request.
402 | Your credits are exhausted. You need to buy credits.
403 | Your provided API key seems to be invalid.
404 | The API endpoint you tried doesn't exist.
405 | The request method you are trying isn't supported on this endpoint.
422 | A validation error occured for some of your query params or form data.
429 | A rare error that tells you that you are making API calls too quickly.
500 | Our fault! Something unexpected happened at our hardware end.
503 | Our services are unavailable (maybe due to an ongoing maintenance).
