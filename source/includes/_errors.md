# Errors

<aside class="notice">
This error section is stored in a separate file in <code>includes/_errors.md</code>. Slate allows you to optionally separate out your docs into many files...just save them to the <code>includes</code> folder and add them to the top of your <code>index.md</code>'s frontmatter. Files are included in the order listed.
</aside>

The Kittn API uses the following error codes:


Error Code | Meaning
---------- | -------
400 | Bad Request -- Your request is invalid.
403 | Your API key seems to be invalid.
405 | The request method you are trying isn't supported on this endpoint.
422 | A validation error occured for some of your query params or form data.
429 | A rare error that tells you that you are making API calls too quickly.
500 | Our fault! Something unexpected happened at our hardware end.
503 | Our services are unavailable (maybe due to an ongoing maintenance).