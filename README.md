#### JavaScript Intermediate/02-asynchronous/01-check-your-knowledge

1. Which of the following is NOT used to create a request using fetch() and explain why?  
Answer: .this() because we use the other three - then() to tell the program what to do after fetching datas, .json() to takes a Response stream and reads it to completion and JSON.stringify() to convert a JavaScript object or value to a string.  
2. A promise is an  
Answer: object  
3. What is wrong with the following code?  
async function getData() {
  try {
    let response = await fetch('https://api-to-call.com/endpoint', { 
      method: 'POST', 
      body: JSON.stringify({id: 200}), 
      dataType: 'json'
  });
  let jsonResponse = await JSON.stringify(response);
  return jsonResponse;
  } catch (error) {
    console.log(error);
  }
}  
Answer:  I tried to run this program but the return value turned out to be an empty value. Icouldn't figure out why tho.  

4. What is wrong with the following code?  
async function getData() {
  try {
    let response = await fetch('https://api-to-call.com/endpoint', 'POST', JSON.stringify({id: 200}), 'json');
    let jsonResponse = await response.json();
    return jsonResponse;
  } catch (error) {
    console.log(error);
  }
}  
Answer: The return value is undefined.

