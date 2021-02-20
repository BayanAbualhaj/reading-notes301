# What I learnd 


![node.js](https://thehackernews.com/images/-1nufw3bQR_s/W_z4WoTfrAI/AAAAAAAAysI/ThbqvRtgAPoCLWAWtZpLCPbKNsqEiRm-QCLcBGAs/s728-e100/nodejs-event-stream-module.jpg)



## Node. js 

* Node Is Built on Google Chrome’s V8 JavaScript Engine : This means that Node.js is a program we can use to execute JavaScript on our computers. In other words, it’s a JavaScript runtime.

* You can check that Node is installed on your system by opening a terminal and typing node -v. If all has gone well, you should see something like v12.14.1 displayed. This is the current LTS version at the time of writing. 


### Introducing npm, the JavaScript Package Manager
1. Installing a Package Globally :This will install the jshint package globally on your system. We can use it to lint the index.js 

2. Installing a Package Locally: We can also install packages locally to a project, as opposed to globally, on our system. Create a test folder and open a terminal in that directory.

3. Working with the package.json File : If you open the package.json file, you’ll see lodash listed under the dependencies field. By specifying your project’s dependencies in this way, you allow any developer anywhere to clone your project and use npm to install whatever packages it needs to run.

### What Is Node.js Used For?

These build tools come in all shapes and sizes, and you won’t get far in a modern JavaScript landscape without bumping into them. They can be used for anything from bundling your JavaScript files and dependencies into static assets, to running tests, or automatic code linting and style checking.

- Node.js Lets Us Run JavaScript on the Server: is the first implementation to gain any real traction, and it provides some unique benefits, compared to traditional languages. 
- The Node.js Execution Model:causes the server very little overhead, and consequently it’s capable of handling a large number of simultaneous connections. 

* The following image depicts Node’s execution model:
![52](https://github.com/BayanAbualhaj/reading-notes301/blob/master/img/Screenshot%20(52).png?raw=true)

-  it can be used as a scripting language to automate repetitive or error prone tasks on your PC. 

- used to write your own command line tool, such as this Yeoman-Style generator to scaffold out new projects.


### Are There Any Downsides?
The fact that Node runs in a single thread does impose some limitations.Some developers also dislike the callback-based style of coding that JavaScript imposes (so much so that there’s even a site dedicated to the horrors of writing asynchronous JavaScript). But with the arrival of native Promises, followed closely by async await, flow control in modern JavaScript has become easier than it ever was.

### What Are the Advantages of Node.js?
1. that your brain no longer needs to switch modes.
2. Node’s big pluses is that it speaks JSON. JSON is probably the most important data exchange format on the Web, and the lingua franca for interacting with object databases (such as MongoDB). 
3. it makes other languages seem cumbersome.



# Quote of the day:

**“You’re building your own maze, in a way, and you might just get lost in it.”**


#### Conclusion
JavaScript is everywhere, and Node is a vast and expansive subject. Nonetheless, I hope that in this article I’ve offered you the beginner-friendly, high-level look at Node.js and its main paradigms that I promised at the beginning. I also hope that when you re-read the definitions we looked at previously, things will make a lot more sense.