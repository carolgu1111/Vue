// source from https://www.youtube.com/watch?v=-Z0i100x0mc

1.let and const
    a.blcok scope
    b.let can be re assign but const is not 

2.shorthand object assignment
    eg
        const name = 'carol';
        const address = 'carol111'

    in old way it should assign as 
        const github = {
            name: name,
            address: address
        }

    but in es6 shorthand way, could be simply as 
        const github = {
            name,
            address
        }
    
3.destrucuring assignment
#object
    const name = {
        first: 'carol',
        last: 'gu'
    }

    old way

        const first = name.first
        const last = name.last

     es6
        const{first,last} = name   
        const{first:f,last:l} = name   

#array
    const name = ['carol','gu']
    old way
        const first = name[0]
        const last = name[1]
    es6
        const[first,last] = name


4.spread syntax
#array/object copy
    const arr = [1,2,3]
    const arrCopy = [...arr]

    const obj = {first:'carol', last:'gu'}
    const objCopy = {...obj}


5.optional chaining
    const person = {
        name:'carol',
        details:{
            age: 99,
            address:{
                city:'catHaven'
            }
        }
    }

    before
        console.log(person.details && person.details.address)
    after
        console.log(person?.details?.address?.city)

6.nullish coalescing operator

    Logical OR
        const name = 'carol'
        const userName = name ||'Guest'
        console.log(userName) // carol

        const name = null
        const userName = name ||'Guest'
        console.log(userName) // Guest

        const name = ''
        const userName = name ||'Guest'
        console.log(userName) // Guest

        const name = 0
        const userName = name ||'N/A'
        console.log(userName) // N/A

    nullish coalescing 
        const name = ''
        const userName = name ??'Guest'
        console.log(userName) // ''

        const name = 0
        const userName = name ??'N/A'
        console.log(userName) // 0


7.ternary operator
    condition ? trueCond: falseCond


8.template literals
    const greeting = 'hello'
    const name = 'carol'
    sport = 'snowboard'

    before
        console.log(greeting + ' ' + name + '. Do you like ' + sport + '?')

    es6
        console.log(`${greeting} ${name}. Do you like ${sport}?`)

9.arrow functions
    traditional
        function greet(){
            console.log('hello')
        }
        function greet(name){
            console.log(`hello ${name}`)
        }
        function getName(){
            return 'carol'
        }

    arrow
        const greet = () => {
            console.log(`hello ${name}`)
        }
        // if single parameter, () is not necessary
        const greet = name => {
            console.log(`hello ${name}`)
        }
        const getName = () => 'carol'

10.import and export
    