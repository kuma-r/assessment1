//1.
    //code:
        var object1={name:"kumar",age:21};
        var object2={name:"kumar",age:21};
        function isEquivalent(a,b) {
            var aProperties = Object.getOwnPropertyNames(a);
            var bProperties = Object.getOwnPropertyNames(b);
        
            if (aProperties.length != bProperties.length) {
                //if both doesnt have same number of properties then it is false
                return "Not Equivalent";
            } 
            for (var i = 0; i < aProperties.length; i++) {
                var propName = aProperties[i];
                if (a[propName] !== b[propName]) {
                    return "Not Equivalent";
                }
            }
            return "Equivalent";
        }
        console.log(`Both objects are ${isEquivalent(object1,object2)}`)
    


//2.
    //A JavaScript class is a type of function. Classes are declared with the class keyword.
    //code:
        class trainer{
            constructor(name,age,sex)
            {
                this.name=name;
                this.age=age;
                this.sex=sex;
            }
            display()
            {
                console.log(`${this.name} ${this.age} ${this.sex}`)
            }
        }
        class trainee extends trainer{
            constructor(name,age,sex,stream,degree){
                super(name,age,sex);
                this.stream=stream;
                this.degree=degree;
            }
            display()
            {
                console.log(`${this.name} ${this.age} ${this.sex} ${this.stream} ${this.degree}`)
            }
        } 

        var t1=new trainer("rahul",25,"male");
        var s1=new trainee("kumar",21,"male","backend","BTech")
        t1.display()
        s1.display()

//3.
    //Destructuring is a JavaScript expression that makes it possible to unpack values from arrays, or properties from objects, into distinct variables.
    //code:
        var array=[1,2,3,4,5];
        var [first,second,third,fourth,fifth]=array;
        console.log(first)
        console.log(second)
        console.log(third)
        console.log(fourth)
        console.log(fifth)

        var testObj={
            one:"kumar is a good boy",
            two:":)"
        }
        var {one,two}=testObj;
        console.log(`${one} ${two}`)

//4.
    //When writing strings in JavaScript, we normally use single ( ‘ ) or double ( “ ).If we want to insert we values we close the string and using + we do it
    //With template literals, we use enclosing back-ticks ( ` ) instead.If we want to insert variable no need to break the string,just use${} to insert the value in between.
    //code
        function Person(name,sex){
            this.name=name;
            if(sex=="m")
            this.sex="boy";
            else
            this.sex="girl";
        }
        var a=new Person("kumar","m")
        var b=new Person("chandana","f")
        console.log(`${a.name} is a good ${a.sex}.`)
        console.log(`${b.name} is a good ${b.sex}.`)
//5.
        var a1=[1,2,3]
        var a2=[1,2,3]
        a2.map(x=>{
            a1.push(x)
        })
        console.log(a1);

//6.
    //RegularExpressions are used to validate format
    //code
        function testing()
        {
        if(regx.test(id))
            return "correct format"
        else
        return "incorrect format"
        }
        var id="kirankumar108k@gmail.com"
        regx=new RegExp("^([a-zA-Z0-9\._]+)@([a-zA-Z_]+).([a-z]{2,5})(.[a-z]{2,5})?$")
        //var regx=/^([a-zA-Z0-9\._]+)@([a-zA-Z_]+).([a-z]{2,5})(.[a-z]{2,5})?$/
        console.log(testing())
            


