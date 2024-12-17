# Functions

## Paramters and Arguments
1. to declare parameter,name and type has to be mentioned.
2. ```bash
    fn open_store(neighbourhood:&str,random:i32){

        println!("Opening my store in {}");
    }
    ```

## Explicit Return values
1. Inorder to declare the return value,we need to add the return keyword.
2. If i am returning something ,I also have to mention the type of the returned value in the function signature.
3. ```bash
    let result=square(34);

    fn square(number:i32)->i32{
        return number*number;
    }

    ```
## Implicit Return values.
1. return keyword will explicitly tell what the returned value is.
2. A function will implicitly returns the last line it evaluates.
3. ```bash
    fn square(number:i32)->i32{
        number*number
    }
    ```

4. See that semi colon should not be kept at the last line.
5. ![alt text](image.png)
6. ![alt text](image-1.png)

## The unit as a return type
1. A unit is an empty typles,a tuple without values.
2. ```bash
    let tup=();
    ```
3. if you see the tyope of tup in the above code,its `()` which is same as the value(empty tuple).
   i.e
    ```bash
    let result:()=emptyfun();
    fn emptyfun(){
    

    }
    ```
4. Thing here is that that tup is same as what the function returns when no return type is mentioned.
5. we can provide void by keeping `->()` but thats not needed.

## Blocks in functions
1. ```bash
    fn main(){
        let multi=34;
        let value_returned_by_blck={
        let value=3;
        value*multi
        };
    }
    ```
2. `{}` gives us an isolated scope/block.
3. **Just like how last line in the function works as returned value,even for block it works the same way**