### Conceptual Exercise

Answer the following questions below:

- What are important differences between Python and JavaScript?

Python is used to develop the backend of web applications while Javascript deals with developing both the back-end and the front end of the application


- Given a dictionary like ``{"a": 1, "b": 2}``: , list two ways you
  can try to get a missing key (like "c") *without* your programming
  crashing.

We can use the get method with a default value.
Value = my_dict.get(key, default_value)


- What is a unit test?

A way of testing the smallest piece of code. Testing code in isolated small pieces.


- What is an integration test?

This is where program  units are combined and tested as groups in multiple ways


- What is the role of web application framework, like Flask?

A structured foundation for building web applications. It simplifies tasks such as routing, request handling etc. it also enhances security, offers templating for separating logic and provides tools for testing. So its a great tool for web developers.


- You can pass information to Flask either as a parameter in a route URL
  (like '/foods/pretzel') or using a URL query param (like
  'foods?type=pretzel'). How might you choose which one is a better fit
  for an application?

  I would pass information as a parameter in a route URL when the information is a fundamental part of the resource being accessed.So something specific. On the other hand I would use the URl query param when the information is optional or used just for filtering, searching or modifying a request. 


- How do you collect data from a URL placeholder parameter using Flask?

From inside a view function, we can access the value of the placeholder parameter as an argument to the function. So when a user accesses a URL with a specific food  for example, flask will pass it in the get food function. The bolded words need to match as well.
from flask import Flask

app = Flask(__name__)

@app.route('/foods/<food_name>')
def get_food(food_name):
    # Access the value of the 'food_name' parameter from the URL
    return f"You requested information about {food_name}"


- How do you collect data from the query string using Flask?

By using the request.args dictionary from the request object in Flask
‘request.args.get(‘parameter_name’)


- How do you collect data from the body of the request using Flask?

For form data in a POST request, use request.form to access form data.
For JSON data in a POST request, use request.get_json() after ensuring the request has a JSON content type.
For other content types or raw data, use request.data to access the raw data.


- What is a cookie and what kinds of things are they commonly used for?

A cookie is a small piece of data stored on a user's device by a web browser.Cookies are commonly used for tasks like session management, user authentication, tracking user preferences, and storing shopping cart information in web applications.


- What is the session object in Flask?

The session object in Flask is a client-side storage mechanism used to store data between multiple requests. It allows web applications to maintain user-specific data across requests, such as user authentication state or shopping cart contents, without relying solely on cookies.

- What does Flask's `jsonify()` do?

jsonify() is a Flask function used to convert Python dictionaries and objects into JSON (JavaScript Object Notation) format.It is commonly used in Flask applications to send structured data as JSON responses to clients, which is useful for building APIs or exchanging data with frontend frameworks.
