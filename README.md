# REST-API
15 problems — description and expected output only:

**Problem 1 — Basic GET request**
Make a GET request to `https://httpbin.org/get` and print the status code and the `url` field from the JSON response.
```
Status: 200
URL: https://httpbin.org/get
```

---

**Problem 2 — Read JSON response**
Make a GET request to `https://httpbin.org/json` and print the title field from the response JSON.
```
Wake up to WonderWidgets!
```

---

**Problem 3 — Query parameters**
Make a GET request to `https://httpbin.org/get` passing `name=Arun` and `city=Chennai` as query parameters. Print the args from the response.
```
{'city': 'Chennai', 'name': 'Arun'}
```

---

**Problem 4 — POST with JSON body**
Send a POST request to `https://httpbin.org/post` with a JSON body containing `title`, `severity`, and `status`. Print the `json` field from the response.
```
{'severity': 'high', 'status': 'open', 'title': 'Login broken'}
```

---

**Problem 5 — Custom headers**
Make a GET request to `https://httpbin.org/headers` passing a custom header `X-Tester-Name: Arun`. Print the `X-Tester-Name` value from the response headers dict.
```
Arun
```

---

**Problem 6 — Auth header**
Make a GET request to `https://httpbin.org/bearer` with a Bearer token in the Authorization header. Print whether the request was authenticated and the token used.
```
Authenticated: True
Token: mytoken123
```

---

**Problem 7 — Status code handling**
Make requests to `https://httpbin.org/status/200`, `https://httpbin.org/status/404` and `https://httpbin.org/status/500`. Print a message for each — success, not found, or server error.
```
200: Success
404: Not found
500: Server error
```

---

**Problem 8 — raise_for_status()**
Make a GET request to `https://httpbin.org/status/404`. Use `raise_for_status()` to catch the error instead of manually checking the status code.
```
HTTP error: 404 Client Error: NOT FOUND for url: https://httpbin.org/status/404
```

---

**Problem 9 — Timeout handling**
Make a GET request to `https://httpbin.org/delay/5` with a timeout of 2 seconds. Handle the timeout exception and print a clean message.
```
Request timed out. Server took too long to respond.
```

---

**Problem 10 — POST form data**
Send a POST request to `https://httpbin.org/post` using `data=` instead of `json=`. Pass `username=arun` and `role=tester`. Print the `form` field from the response.
```
{'role': 'tester', 'username': 'arun'}
```

---

**Problem 11 — Response headers**
Make a GET request to `https://httpbin.org/get` and print the `Content-Type` value from the response headers.
```
application/json
```

---

**Problem 12 — PUT request**
Send a PUT request to `https://httpbin.org/put` with a JSON body updating a bug status. Print the `json` field from the response.
```
{'id': 42, 'status': 'closed'}
```

---

**Problem 13 — DELETE request**
Send a DELETE request to `https://httpbin.org/delete` with a JSON body containing an `id`. Print the `json` field confirming what was deleted.
```
{'id': 7}
```

---

**Problem 14 — Reusable API client class**
Create an `APIClient` class with a `base_url` and optional `token`. Add a `get(endpoint)` method that automatically adds the auth header if token is provided, and a `post(endpoint, payload)` method. Use `https://httpbin.org` as base.
```
Status: 200
Authenticated: True
```

---

**Problem 15 — Chain two API calls**
Make a GET request to `https://httpbin.org/uuid` to get a unique ID. Then immediately make a POST request to `https://httpbin.org/post` sending that UUID as `request_id` in the body. Print the `request_id` from the POST response.
```
Got UUID: <some-uuid>
Posted request_id: <same-uuid>
```

---
