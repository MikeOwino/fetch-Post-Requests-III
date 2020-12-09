# fetch-Post-Requests-III

In the previous exercise, you created the boilerplate code for making a POST request using fetch() and .then(). In this exercise, you’re going to update that boilerplate code to allow you to shorten a URL using the Rebrandly URL Shortener API.

Rebrandly API.
If you haven’t already created a Rebrandly API key, read through the Rebrandly sign up guide:

Codecademy Articles: Rebrandly URL Shortener API.
Keep in mind, while it’s ok to use your API key in these exercises, you should not share your key with anyone (not even if asking a question in the forums)! Also, if you reset the exercise at any point, you will have to paste in your API key again at the top.

Instructions
1.
Assign apiKey to your Rebrandly API key as a string.

If you do not assign the correct key, you will not see the proper results in the steps afterwards.

Checkpoint 2 Passed

Hint
You can find const apiKey at the top of main.js replace '<Your API Key>' with your actual Rebrandly API key.

2.
Inside the code block of shortenUrl(), create a const named urlToShorten and assign it inputField.value. urlToShorten will keep the value of what is being typed into the input field.

Please note, you will be working inside shortenUrl() for the remainder of this exercise.

Checkpoint 3 Passed

Hint
Make sure you’re working inside shortenUrl().

3.
Underneath urlToShorten, create another const named data, and assign it to the result of calling the method JSON.stringify() with {destination: urlToShorten} as an argument.

The reason for creating data is to prepare the information needed to send in the body.

Checkpoint 4 Passed

Hint
First create a const named data

const data  
Then assign data to the value of the result of calling JSON.stringify() and passing in {destination: urlToShorten}

const data = JSON.stringify({destination: urlToShorten})
4.
Below data, call the fetch() function. Pass it url as its first argument and an empty object as its second argument.

Checkpoint 5 Passed

Hint
The syntax for this step would look something like:

fetch(url, {})
5.
Now it’s time to add some properties to the empty object that you just created. Create a property with the key method and the value 'POST'.

Checkpoint 6 Passed

Hint
Make sure you’re in the empty object you created in the previous step.

An object with a single property (key-value pair) should look like this:

{ exampleKey: 'example value' }
6.
In the same object, create another property. The key for this property is headers and the value will be another object.

Assign headers the value of another object listed below:

{
  'Content-type': 'application/json',
  'apikey': apiKey
}
Checkpoint 7 Passed

Hint
Separate the properties using commas.

In this step you have to create an object inside an object! Take a look at the following example:

let someObject = {
  key1: value1,
  key2: {
    insideKey2: valueInsideKey2,
    alsoInsideKey2: value2InsideKey2
  }
}
7.
In that same object that has the properties method and headers, add another property. The key is named body and the value will be data.

Setting up this information now will make chaining .then() in the next exercise much easier!

Checkpoint 8 Passed

Hint
Make sure you’re adding it to the object that has method and headers. You’re not in the headers object.

Also, check to see that you’ve separated the properties with commas. In this step, you’re creating another key-value pair.

The syntax for the object will look similar to:

let someObject = {
  method: value1,
  headers: {
    insideKey2: valueInsideKey2,
    alsoInsideKey2: value2InsideKey2
  },
  key3: value3 
}
