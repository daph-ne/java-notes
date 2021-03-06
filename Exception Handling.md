EXCEPTION HANDLING

Exception:
    * An abnormal condition that arises in a code sequence at run time.
    * When an exceptional condition arises, an object representing the exception is created and thrown in the method that caused the error.

5 keywords in java exception handling:
    1. try
        * Programs you want to monitor for exception are contained within a try block.
    2. catch
        * This catches the exception which is thrown and handles it in some rational manner.
    3. throw
        * throw is used to manually throw an exception.
    4. throws
        * Any exception that is thrown out of a method must be specified as such by a throws clause.
    5. finally
        * Any code that absolutely must be executed after a try block completes is put in a finally block.

Exception Types
    * All exception types are subclass of the built-in class Throwable.
    Throwable has 2 sub-classes:
        1. Exception
        2. Error
    
Benefits of using try and catch:
    1. Allows to fix the error
    2. Prevents the program from automatically terminating



