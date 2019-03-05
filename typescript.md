# Typescript

## General

http://www.typescriptlang.org/docs/home.html

## Type declarationd

* Define a variable as a string

    ``` typescript
    let myString: string
    ```

* Other types

    ``` typescript
    let myNumber: number;
    let myBoolean: boolean;
    let myArray: Array<string>:
    let anything: any;
    ```

* This is also infered if you assign a variable as a string  

    ``` typescript
    let myString = 'This is my string'
    ```

    The type is only infered if a value is set to the varible at declaration.

## Classes

* Define type return value

    ``` typescript
      getEndpointName(): string {
         return 'android';
      }
    ```

## Interfaces

* Declare interface

    ```typescript
    interface User {
        username: string;
        password: string:
        confirmPassword?: string
    }
    ```

    The questionmark indicates an optional property