```mermaid
classDiagram
    direction BT %% TB, BT, RL, LR 모두 가능
    clss Person{
        <<abstract>>
        +name:str
        +phoneNumber: str
        +emailAddress: str
        +purchaseParkingPass()
    }

    class Student{
        +studentNumber: int
        +avarageMark: int
        +isEligibleToEnroll(str) boll
        +getSeminarsTaken(): int
    }

    class Professor{
        -salary: int
        #staffNumber: int
        -yearsOfService: int
        +numberOfClaseses: int
    }

    class Address{
        +street: str
        +city: str
        +state: str
        +postalCode: int
        +country: str
        -validate() bool
        +outputAsLabel() str
    }

    person <\-- Student
    Person <\-- Professor
    Student "0..*"<--"1..5" professor : supervise
    Person "0..1"-->"1" Address : lives in
```

