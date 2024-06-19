## 1. Introduction to Postman Tests

### Overview
Postman tests are written in JavaScript and executed after a request is made to validate the response. Tests can check status codes, response times, response bodies, and more.

### Accessing the Tests Tab
In Postman, each request has a "Tests" tab where you can write your test scripts. These scripts run after the request is completed.

---

## 2. Writing Basic Tests

### Structure of a Test
Postman provides a simple syntax to write tests using `pm.test` and `pm.expect`.

```javascript
pm.test("Test name", function () {
    pm.expect(responseCode.code).to.eql(200);
});
```

Example: Checking Response Status

```javascript
pm.test("Status code is 200", function () {
    pm.expect(pm.response.code).to.eql(200);
});
```

## 3. Validating Response Status Codes
Checking for Specific Status Codes
You can validate that the API returns the expected status code.

```javascript
pm.test("Status code is 200", function () {
    pm.expect(pm.response.code).to.eql(200);
});
```
