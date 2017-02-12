# mealOrderCalculator
Notes and Assumnptions

NOTES

1) The program was written in Visual Studio .NET as a C# Console application.
2) The input is a .txt file with the following format
    Order
    Total:< #meals >
    < #1 special meal type: quanity >
    < #2 special meal type: quanity >
    ...
    < #n special meal type: quanity >
    
    Restaurant A
    Rating:< rating >
    Total:< #meals >
    < #1 special meal type: quanity >
    < #2 special meal type: quanity >
    ...
    < #n special meal type: quanity >
    
    Restaurant B
    Rating:< rating >
    Total:< #meals >
    < #1 special meal type: quanity >
    < #2 special meal type: quanity >
    ...
    < #n special meal type: quanity >
    
3) The output is a text file saved in the same directory as the input with ".out" added after the txt extension. It has the following format

    Restaurant A
    Rating:< rating >
    Total:< #meals >
    < #1 special meal type > < quanity >
    < #2 special meal type > < quanity >
    ...
    < #n special meal type > < quanity >
    Others < quantity >
    
    Restaurant B
    Rating:< rating >
    Total:< #meals >
    < #1 special meal type > < quanity >
    < #2 special meal type > < quanity >
    ...
    < #n special meal type > < quanity >
    Others < quantity >
    
4) Sample input and output files are included with the solution
    
ASSUMPTIONS

1) The special meal types (Vegetarian, Gluten Free) are all exclusive, even if in reality they aren't. So even though a Vegetarian could eat anything a Vegan could, the program would not see it this way.

2) The orders that do not require restriction can be satisfied with special meals. For example if 8 meals are ordered of which 4 should be vegetarian, and Restaurant A has 8 total orders of which 4 are vegetarian, and 4 are gluten free, then the for non vegetarian meals in the order can be taken from the 4 gluten free orders in the reataurant. It was assumed that this is how the program should behave since otherwise the "Other" meals or meals without restrictions could just be treated as another special meal category called "Others".

3) The ':' character is used as a separator in the input text file and should not be used as a part of any restaurant or special meal name.

4) Empty lines are used to separate orders and restaurants in the input text file and should not be used otherwise.

5) If the number of total meals ordered is more than the sum of meals available at all restaurant. The program order will not be fulfilled. The program will only take a number of meals equal to the sum of available meals at all restaurants

6) If the total number of a particular special meal ordered is more than the sum of meals of that type available in all restaurants, the prgram will fill this orders with regular "Other" meals.
  
    
    
    
