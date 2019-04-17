# fizzbuzz_js_BOA
#1
let  fizzBuzz = fs.readFileSync('./src/js/fizz-buzz.js');
eval( fizzBuzz + `\nexports.FizzBuzz = FizzBuzz;`)

A: let - It reads the the files sources from fizz-buzz
   eval( +  `\nexports ) - adds modulos to our fizz-buzz



#2 Use best of your knowledge to please explain why we are placing the let fizzBuzz = new FizzBuzz outside the it block?

     A: Because it's a part of the function description and it must be accessible to thr block. 



#3. In your README to the best of your knowledge please explain the difference between using === and == in JS?
 
      A: Triple equals( === ) in JavaScript are testing for strict equality.  This means both the type and the value we are         comparing have to be the same. 

      While  Double equails( == ) are testing for loose equality. It means, for example, 7 == "7" doesn't have to be strictly       equal.
  
  
#4. In your README to the best of your knowledge please explain why we are moving (number % 5 === 0) to the top?
 
 

#5 In your README to the best of your knowledge please explain the difference between feature and unit test.
 
 While both feature and unit test are vital for our work as Programmers. Both tests are slightlly firenten. 
 Feature test focus more in user friendly sactisfactions/expectations, the  Unit test is strickly for the testing those small pieces of data that will make the user experiencie possible.


#6 In your README to the best of your knowledge please explain what this following code does

describe('User can input a value and get FizzBuzz results', () => {
    before(async () => {
        await  browser.init()
        await  browser.visitPage('http://localhost:8080/')
    });

    beforeEach(async () => {
        await  browser.page.reload();
    })

    after(async ()=> {
        await  browser.close();
    })
})

A: It basically does open and close our browser during our testing enviroment. 

#7 it('clicking on the "Check" button', async () => {
    await browser.fillIn("input[id='value']", { with:  "3" })
    await browser.clickOnButton("input[value='Check']")
    let content = await browser.getContent("[id='display_answer']")
    expect(content).to.eql('Fizz');
    })
 A: We are expecting the result of we are asking for to be equal when the conditions are met!
 
 
 #8. In your README to the best of your knowledge please write a line to line explanation of what is happening in this code

<script src="./js/fizz-buzz.js"></script>
    <script>
        document.addEventListener('DOMContentLoaded', () => {
            let button = document.getElementById('button')
            let displayDiv = document.getElementById('display_answer')
            button.addEventListener('click', () =>{
                let value = document.getElementById('value').value
                let fizzBuzz = new FizzBuzz
                let result = fizzBuzz.check(value)
                displayDiv.innerHTML = result;
            })
        })
    </script>
    
    
    A: Here is DOM doing his magic! When it is loaded with content from our src, it expels whatever is asked and available. 
    In this case, we imput(ask) some info and the the 'Listerners gives us the values(info) we are expecting. 
    
    #9. In your README to the best of your knowledge please explain what a CDN (Content Delivery Network) is?
    
       A: CDN is a globally distributed network of web servers whose purpose is to provide faster delivery, and highly available content.
