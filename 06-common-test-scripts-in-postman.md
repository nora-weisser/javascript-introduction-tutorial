## 1. Introduction to Postman Tests

### Overview
Postman tests are written in JavaScript and executed after a request is made to validate the response. Tests can check status codes, response times, response bodies, and more.

### Accessing the Scripts Tab
You can add JavaScript code to execute during two events in the flow:

1. Before a request is sent to the server, as a pre-request script under the **Scripts** > Pre-request tab.
2. After a response is received, as a post-response script under the Scripts > Post-response tab.

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

## 3. Common Test Validations
### Status Code Validation
Checking for Specific Status Codes
You can validate that the API returns the expected status code.

```javascript
pm.test("Status code is 200", function () {
    pm.expect(pm.response.code).to.eql(200);
});
```

### Response Time Validation

```javascript
// Test if the response time is less than 500ms
pm.test("Response time is within acceptable range", function () {
    pm.expect(pm.response.responseTime).to.be.below(500);
});
```

### Response Body Validation

```javascript
// Test if the response body contains a specific value
pm.test("Response body contains expected data", function () {
    pm.expect(pm.response.text()).to.include("expected_value");
});
```

### JSON Response Validation

```javascript
// Test if the response is a valid JSON
pm.test("Response is valid JSON", function () {
    pm.expect(pm.response.json()).to.be.an("object");
});
```

### Header Validation

```javascript
// Test if a specific header is present in the response
pm.test("Header is present in the response", function () {
    pm.response.to.have.header("header_name");
});
```

### Chaining Tests

```javascript
// Chaining multiple test assertions
pm.test("Chaining multiple assertions", function () {
    pm.expect(pm.response.json().property1).to.eql("value1");
    pm.expect(pm.response.json().property2).to.eql("value2");
});
```

### Dynamic Data Validation

```javascript
// Test if a specific value in the response matches the environment variable
pm.test("Dynamic data validation", function () {
    pm.expect(pm.response.json().user_id).to.eql(pm.environment.get("user_id"));
});
```

### Setting data from the environment variable

```javascript
var jsonData = pm.response.json();
pm.environment.set("companyIdToDelete", jsonData.data._id);
```

### Retrieve the current Value of the Variable

```javascript
//access a variable at any scope including local
pm.variables.get("variable_key");
//access a global variable
pm.globals.get("variable_key");
//access a collection variable
pm.collectionVariables.get("variable_key");
//access an environment variable
pm.environment.get("variable_key");
```

### Response Schema Validation

**JSON Schema** is a vocabulary that allows you to annotate and validate JSON documents. It describes your existing data format with clear, human- and machine-readable documentation for complete structural validation, useful for automated testing and validating client-submitted data.

You can use a JSON schema to construct a model of your API response and validate the response of an API call, ensuring that the values in API responses are valid in terms of type and format.

```javascript
// Test if the response adheres to a specific JSON schema
pm.test("Response schema validation", function () {
    const schema = {
        "type": "object",
        "properties": {
            "property1": { "type": "string" },
            "property2": { "type": "number" }
        }
    };
    pm.expect(tv4.validate(pm.response.json(), schema)).to.be.true;
});
```
