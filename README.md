# TestRestrictContactByName
Test class for apex trigger to clear trailhead challenge 'TestRestrictContactByName'

The challenge was follows

Create a Unit Test for a Simple Apex Trigger
Create and install a simple Apex trigger which blocks inserts and updates to any contact with a last name of 'INVALIDNAME'. You'll copy the code for the class from GitHub. Then write unit tests that achieve 100% code coverage.
Create an Apex trigger on the Contact object
Name: RestrictContactByName
Code: Copy from GitHub
Place the unit tests in a separate test class
Name: TestRestrictContactByName
Goal: 100% test coverage
Run your test class at least once

Bellow code will work for the challenge:

@isTest
private class TestRestrictContactByName{
   private static testmethod void restrictContactByNameTest(){
       Contact cont = new Contact();
       cont.FirstName = 'NewContact';
       cont.LastName = 'INVALIDNAME';
       insert cont;
       cont.FirstName = 'NewContact1122';
       cont.LastName = 'INVALIDNAME1122';
       insert cont;
   }
}

