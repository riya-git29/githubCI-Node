node-CLI
    .github/
        workflow/
            node-ci.yaml
    tests/
        math.test.js 
    math.js
    package.json
    README.md 

math.js 
function add(a,b){
    return a+b;
}
function sub(a,b){
    return a-b;
}
module.exports={add,sub};

math.test.js 
const {add,subtract} =require('../math');


test('add',()=>{
    expect(add(2,3)).toBe(5);
})
test('add',()=>{
    expect(add(2,1)).toBe(1);
})

node-ci.yaml
name: Node.js CI 
on:
    push:
    branches:[main]
    pull_request:
    branches:[main]

jobs:
    build:
        run-on:ubuntu-latest

        steps:
            -name:Checkout code 
            uses: actions/checkout@v3

            -name :Set up node js 
            uses: actions/setup-node@v3
            with 
            node-version:'18'

            -name: Install dependencies
            run : npm Install
            -name: Run tests
            run : npm test
