Download Link: https://assignmentchef.com/product/solved-comp1210-project-10-bakery-part-2
<br>
<h1>Deliverables</h1>

Your project files should be submitted to Web-CAT by the due date and time specified.  Note that there is also an optional Skeleton Code assignment this week which will indicate level of coverage your tests have achieved (there is no late penalty since the skeleton code assignment is ungraded for this project).  The files you submit to skeleton code assignment may be incomplete in the sense that method bodies have at least a return statement if applicable or they may be essentially completed files.  In order to avoid a late penalty for the project, you must submit your <u>completed code</u> files to Web-CAT no later than 11:59 PM on the due date for the completed code.  You may submit your <u>completed code</u> up to 24 hours after the due date, but there is a late penalty of 15 points.  No projects will be accepted after the one-day late period.  If you are unable to submit via Web-CAT, you should e-mail your project Java files in a zip file to your TA before the deadline. The Completed Code will be tested against your test methods in your JUnit test files and against the usual correctness tests.  The grade will be determined, in part, by the tests that you pass or fail and the level of coverage attained in your Java source files by your test methods.




Files to submit to Web-CAT:

<u>From Bakery – Part 1</u>

<ul>

 <li>java</li>

 <li>java, CookieTest.java</li>

 <li>java, PieTest.java</li>

 <li>java, CakeTest.java</li>

 <li>java, WeddingCakeTest.java</li>

</ul>

<u>New in Bakery – Part 2</u>

<ul>

 <li>java, PriceComparatorTest.java</li>

 <li>java, FlavorComparatorTest.java</li>

 <li>java, BakedItemListTest.java</li>

 <li>java, BakeryPart2Test.java</li>

</ul>

<strong> </strong>

<h1>Recommendations</h1>

You should create a new folder for Part 2 and copy your relevant Part1 source and test files to it. You should create a jGRASP project and add the class and test files as they are created. <strong> </strong>

<strong> </strong>

<strong>Specifications – </strong><strong>Use arrays in this project; ArrayLists are not allowed! </strong>

<strong>Overview</strong>:  This project is Part 2 of three that involves a bakery and reporting for baked items.  In Part 1, you developed Java classes that represent categories of baked items including cookies, pies, cakes, and wedding cakes.  In Part 2, you will implement four additional classes: (1)

PriceComparator, which implements the Comparator interface to compare baked items by price; (2)

FlavorComparator, which implements the Comparator interface to compare baked items by flavor; (3)

BakeryItemList, which represents a list of baked items and includes several specialized methods; and

(4) BakeryPart2, which contains the main method for the program.   Note that the main method in BakeryPart2 should declare a BakeryItemList object and then call the readItemFile method which will add baked items to the BakeryItemList as the data is read in from a file.  You can use BakeryPart2 in conjunction with interactions by running the program in the canvas (or debugger with a breakpoint) and single stepping until the variables of interest are created.  You can then enter interactions in the usual way. In addition to the source files, you will create a JUnit test file for each class and write one or more test methods to ensure the classes and methods meet the specifications.  <u>You should create a</u> <u>jGRASP project upfront and then add the source and test files as they are created.  All of your files</u> <u>should be in a single folder</u>.

<strong> </strong>

<ul>

 <li><strong>Cookie, Pie, Cake, and WeddingCake </strong></li>

</ul>

<strong> </strong>

<strong>Requirements and Design</strong>: No changes from the specifications in Part 1.




<ul>

 <li><strong>java           </strong></li>

</ul>

<strong>                </strong>

<strong>Requirements and Design</strong>: <u>In addition to the specifications in Part 1</u>, the BakedItem class should implement the Comparable interface for BakedItem, which means the following method must be implemented in BakedItem.

o compareTo:  Takes a BakedItem as a parameter and returns an int indicating the ordering from <u>lowest to highest</u> based on the class name followed <em>name</em>, and <em>flavor</em>. Since this is essentially the same as the toString value, you could do the compareTo based on toString value.  Otherwise, to do this, you will need to extract the class name, <em>name</em>, and<em> flavor </em>from the BakedItem and do the compareTo based these.  Regardless of the method you use, to avoid uppercase and lowercase issues you should make the String values either all uppercase or all lowercase prior to comparing them.




<ul>

 <li><strong>java </strong></li>

</ul>




<strong>Requirements: </strong>The BakedItemList class provides methods for reading in the data file and generating reports.

<strong> </strong>

<strong>Design: </strong>The BakedItemList class has fields, a constructor, and methods as outlined below.




<ul>

 <li><strong>Fields:</strong> All fields below should be private.

  <ul>

   <li><em>listName</em> is the name of the BakedItemList.</li>

   <li><em>itemList</em> is an array that can hold up to 100 BakedItem objects.</li>

   <li><em>itemCount</em> tracks the number of BakedItem objects in the <em>itemList</em></li>

   <li><em>excludedRecords</em> is an array that can hold up to 30 String elements representing records that are read from the data file but not processed.</li>

   <li><em>excludedCount</em> tracks the number of records that have been added to the excludedRecords array.</li>

   <li>listCount is a <u>static</u> field initialized to zero, which tracks the number of BakedItemList objects created.</li>

  </ul></li>

</ul>




<ul>

 <li><strong>Constructor: </strong>The constructor has no parameters, initializes the instance fields in BakedItemList, and increments the static field listCount. The readItemFile method defined below will populate the BakedItemList object.</li>

 <li><strong>Methods:</strong> Usually a class provides methods to access and modify each of its instance variables (i.e., getters and setters) along with any other required methods. The methods for BakedItemList are described below.

  <ul>

   <li>getListName returns the String representing the listName.</li>

   <li>setListName has no return value, accepts a String, and then assigns it to listName. o getItemList returns the BakedItem array representing the <em>itemList</em>.</li>

   <li>setItemList has no return value, accepts a BakedItem array, and then assigns it to <em>itemList</em> (used in conjunction with setItemCount to provide a new BakedItem array and <em>itemCount</em>).</li>

   <li>getItemCount returns the current value of <em>itemCount</em>.</li>

   <li>setItemCount has no return value, accepts an int, and assigns it to <em>itemCount</em>. o getExcludedRecords returns the String array representing the excludedRecords. o setExcludedRecords has no return value, accepts a String array, and then assigns it to excludedRecords (used in conjunction with setExcludedCount to provide a new excluded records array and new excluded records count).</li>

   <li>getExcludedCount returns the current value of excludedCount. o setExcludedCount has no return value, accepts an int, and sets excludedCount to it.</li>

   <li>getListCount is a <u>static</u> method that returns the current value of listCount.</li>

   <li>resetListCount is a <u>static</u> method that has no return value and sets listCount to 0.</li>

   <li>readItemFile has no return value and accepts the data file name as a String.</li>

  </ul></li>

</ul>

Remember to include the throws IOException clause in the method declaration. This method creates a Scanner object to read in the file, and then reads the file line by line.  The first line contains the BakedItemList name and each of the remaining lines contains the data for a baked item.  After reading in the list name, the “baked item” lines should be processed as follows.  A baked item <u>line</u> is read in, a second scanner is created on the <u>line</u>, and the individual values for the baked item are read in.  After the values on the line have been read in, an “appropriate” BakedItem object is created. The data file is a “comma separated values” file; i.e., if a line contains multiple values, the values are delimited by commas.  So when you set up the scanner for the baked item lines, you need to set the delimiter to use a “,” by calling the useDelimiter(“,”) method on the Scanner object.   Each baked item line in the file begins with a category for the baked item (C, P, K, and W are valid categories for baked items indicating <strong>C</strong>ookie, <strong>P</strong>ie, <strong>K</strong> for Cake, and <strong>W</strong>eddingCake respectively).  The second field in the record is the name, followed by flavor, weight, and quantity.  The next field(s) may correspond, as appropriate, to the data needed for the particular category (or subclass) of BakedItem (e.g., a Pie has a crustCost and a Cake has layers). The last fields are the ingredients, which should be stored in an array (new String[50]) as they are read in. After all ingredients have been read in, use the java.util.Arrays copyOf method make a new ingredients array with length equal to the number of ingredients. If the line/record has a valid category and it has been successfully read in, the appropriate BakedItem object should be created and added to itemList.  If an item line has an invalid category, no BakedItem is created and the line should be added to the excluded records array with the

String “*** invalid category *** for line:
” appended to the front of it, and the excuded count should be incremented. The file <em>baked_item_data.csv</em> is available for download from the course web site.  Below are example data records (the first line/record containing the BakedItemList name is followed by baked item lines/records):




Auburn’s Best Bakery

C,Chips Delight,Chocolate Chip,12,flour,sugar,dark chocolate chips,butter,baking soda,salt D,Chips Delight,Chocolate Chip,12,flour,sugar,dark chocolate chips,butter,baking soda,salt

P,Weekly Special,Apple,1,0,flour,sugar,apple,cinnamon,butter,baking soda,salt

R,Weekly Special,Apple,1,0,flour,sugar,apple,cinnamon,butter,baking soda,salt

P,Summer Special,Key Lime,1,2.0,flour,sugar,lime juice,lemon juice,graham crackers,butter,baking soda,salt

K,Birthday,Chocolate,1,1,flour,sugar,cocoa powder,vanilla,eggs,butter,baking soda,baking powder,salt

K,2-Layer,Red Velvet,1,2,flour,sugar,cocoa powder,food coloring,eggs,butter,baking soda,baking powder,salt W,3-Layer/3-Tier,Vanilla,1,3,3,flour,sugar,buttermilk,coffee,eggs,butter,baking soda,baking powder,salt

o generateReport processes the item list array using the <u>original order</u> from the file to produce the bakery Report which is returned as a String.  See the example output on pages 7 – 8.

<ul>

 <li>generateReportByClass makes a copy of the item list array and sorts the copy using the <u>natural ordering</u>, and processes the sorted array to produce the bakery Report (by Class) which is returned as a String. See the example output on pages 7 – 9.</li>

 <li>generateReportByPrice makes a copy of the item list array and sorts the copy <u>by</u> <u>item price</u>, and processes the sorted array to produce the bakery Report (by Price) which is returned as a String. See the example output on pages 7 – 8.</li>

 <li>generateReportByFlavor makes a copy of the item list array and sorts the copy <u>by flavor</u>, and processes the sorted array to produce the bakery Report (by Flavor) which is returned as a String. See the example output on pages 7 – 8.</li>

 <li>generateExcludedRecordsReport processes the excludedRecords array to produce the Excluded Records Report which is returned as a String. See the example output on pages 7 – 8.</li>

</ul>

<strong> </strong>

<strong>Code and Test:  </strong>See examples of file reading and sorting (using Arrays.sort) in the class notes.

The natural sorting order for BakedItem objects is determined by the compareTo method from the Comparable interface.  If <em>itemList</em> is the variable for the array of BakedItem objects, it can be sorted with the following statement.

BakedItem[] bList = Arrays.copyOf(itemList, itemCount);

Arrays.sort(bList);




The sorting order based on item price is determined by the PriceComparator class which implements the Comparator interface (described below).  It can be sorted with the following statement.<strong>         </strong>

BakedItem[] bList = Arrays.copyOf(itemList, itemCount);

Arrays.sort(bList, <strong>new</strong> PriceComparator());

The sorting order based on boarding cost is determined by the FlavorComparator class which implements the Comparator interface (described below).  It can be sorted with statements similar to those above, except that a new FlavorComparator is passed to the Arrays.sort method.




<ul>

 <li><strong>java </strong></li>

</ul>

<strong> </strong>

<strong>Requirements and Design: </strong>The PriceComparator class implements the Comparator interface for BakedItem objects.  Hence, it implements the following method.




<ul>

 <li>compare(BakedItem b1, BakedItem b2)that defines the ordering from <u>lowest</u> <u>to highest</u> based on the price of the baked item.</li>

</ul>




Note that the <em>compare</em> method is the only method in the PriceComparator class.  An instance of this class will be used as one of the parameters when the Arrays.sort method is used to sort by “price”.  For an example of a class implementing Comparator, see class notes on Comparing Objects.




<ul>

 <li><strong>java </strong></li>

</ul>

<strong> </strong>

<strong>Requirements and Design: </strong>The FlavorComparator class implements the Comparator interface for BakedItem objects.  Hence, it implements the following method.




<ul>

 <li>compare(BakedItem b1, BakedItem b2)that defines the ordering from</li>

</ul>

<u>highest to lowest</u> (i.e., alphabetical order, ignoring case) based on the flavor of each baked item.




Note that the <em>compare</em> method is the only method in the FlavorComparator class. An instance of this class will be used as one of the parameters when the Arrays.sort method is used to sort by “flavor”.  For an example of a class implementing Comparator, see class notes on Comparing Objects.

<strong> </strong>

<ul>

 <li><strong>BakeryPart2</strong><strong>.java </strong></li>

</ul>

<strong> </strong>

<strong>Requirements and Design: </strong>The BakeryPart2 class has only a main method as described below.   o main reads in the file name as the first argument, args[0], of the command line arguments, creates an instance of BakedItemList, and then calls the readItemFile method in the BakedItemList class to read in the data file and generate the five reports as shown in the output examples beginning on page 7.  If no command line argument is provided, the program should indicate this and end as shown in the first example output on page 7.  An example data file, <em>baked_item_data.csv </em>can be downloaded from the Lab assignment web page, and this file will be available in Web-CAT for use with your test files.  Any .csv data files that you create for your test methods will need to be uploaded to Web-CAT along with your source and test files. <strong> </strong>




<strong>Code and Test:  </strong>In your JUnit test file for the BakeryPart2 class, you should have at least two test methods for the main method.  One test method should invoke BakeryPart2.main(args) where args is an empty String array, and the other test method should invoke BakeryPart2.main(args) where args[0] is the String representing the data file name. Depending on how you implemented the main method, these two test methods should cover the code in main. In the first test method, you should reset <em>listCount</em>, call your main method, then assert that getListCount()is <u>zero</u> for the test with no file name.  In the second test method, you should reset <em>listCount</em>, call your main method assert that getListCount()is <u>one</u> with <em>baked_item_data.csv </em>as the file name passed in as args[0].

<strong> </strong>

In the first test method, you can invoke main with no command line argument as follows:

// You should be checking for args.length == 0

// in BakeryPart2, and the following should exercise

// the code for true.

BakedItemList.resetListCount();

String[] args1 = {};  // an empty String[]

BakeryPart2.main(args1);

Assert.assertEquals(<strong>“</strong><strong>Baked Item List </strong><strong>count should be 0. “</strong>,

0, BakedItemList.getListCount());

In the second test method, you can invoke main as follows with the file name as the first (and only) command line argument:

BakedItemList.resetListCount();

String[] args2 = {<strong>“baked_item_data.csv”</strong>};

// element args2[0] is the file name

BakeryPart2.main(args2);

Assert.assertEquals(<strong>“</strong><strong>Baked Item List </strong><strong>count should be 1. “</strong>,

1, BakedItemList.getListCount());




If Web-CAT complains that the default constructor for BakeryPart2 has not been covered, you should include the following line of code in one of your test methods.

// to exercise the default constructor  BakeryPart2 app = <strong>new</strong> BakeryPart2();

<strong> </strong>

<strong> </strong>




<h1>Example Output when no file name is provided as a command line argument</h1>

—-jGRASP exec: java BakeryPart2

File name expected as command line argument.

Program ending.




—-jGRASP: operation complete.

<strong> </strong>

<h1>Example Output when <em>baked_item_data.csv </em>is the command line argument</h1>

<table width="639">

 <tbody>

  <tr>

   <td width="639"> —-jGRASP exec: java BakeryPart2 baked_item_data.csv—————————————Report for Auburn’s Best Bakery————————————— Cookie: Chips Delight – Chocolate Chip   Quantity: 12   Price: $4.20 (Ingredients: flour, sugar, dark chocolate chips, butter, baking soda,  salt) Pie: Weekly Special – Apple   Quantity: 1   Price: $12.00 (Ingredients: flour, sugar, apple, cinnamon, butter,  baking soda, salt) Pie: Summer Special – Key Lime   Quantity: 1   Price: $14.00(Ingredients: flour, sugar, lime juice, lemon juice, graham crackers,  butter, baking soda, salt) Cake: Birthday – Chocolate   Quantity: 1   Price: $8.00 (Ingredients: flour, sugar, cocoa powder, vanilla, eggs,  butter, baking soda, baking powder, salt) Cake: 2-Layer – Red Velvet   Quantity: 1   Price: $16.00 (Ingredients: flour, sugar, cocoa powder, food coloring, eggs,  butter, baking soda, baking powder, salt) WeddingCake: 3-Layer/3-Tier – Vanilla   Quantity: 1   Price: $135.00(Ingredients: flour, sugar, buttermilk, coffee, eggs,  butter, baking soda, baking powder, salt)  —————————————Report for Auburn’s Best Bakery (by Class)————————————— Cake: 2-Layer – Red Velvet   Quantity: 1   Price: $16.00 (Ingredients: flour, sugar, cocoa powder, food coloring, eggs,  butter, baking soda, baking powder, salt) Cake: Birthday – Chocolate   Quantity: 1   Price: $8.00 (Ingredients: flour, sugar, cocoa powder, vanilla, eggs,  butter, baking soda, baking powder, salt) Cookie: Chips Delight – Chocolate Chip   Quantity: 12   Price: $4.20 (Ingredients: flour, sugar, dark chocolate chips, butter, baking soda,  salt)Pie: Summer Special – Key Lime   Quantity: 1   Price: $14.00(Ingredients: flour, sugar, lime juice, lemon juice, graham crackers,  butter, baking soda, salt) Pie: Weekly Special – Apple   Quantity: 1   Price: $12.00 (Ingredients: flour, sugar, apple, cinnamon, butter,  baking soda, salt) WeddingCake: 3-Layer/3-Tier – Vanilla   Quantity: 1   Price: $135.00(Ingredients: flour, sugar, buttermilk, coffee, eggs,  butter, baking soda, baking powder, salt)  </td>

  </tr>

  <tr>

   <td width="639">—————————————Report for Auburn’s Best Bakery (by Price)————————————— Cookie: Chips Delight – Chocolate Chip   Quantity: 12   Price: $4.20 (Ingredients: flour, sugar, dark chocolate chips, butter, baking soda,  salt) Cake: Birthday – Chocolate   Quantity: 1   Price: $8.00 (Ingredients: flour, sugar, cocoa powder, vanilla, eggs,  butter, baking soda, baking powder, salt) Pie: Weekly Special – Apple   Quantity: 1   Price: $12.00 (Ingredients: flour, sugar, apple, cinnamon, butter,  baking soda, salt) Pie: Summer Special – Key Lime   Quantity: 1   Price: $14.00(Ingredients: flour, sugar, lime juice, lemon juice, graham crackers,  butter, baking soda, salt) Cake: 2-Layer – Red Velvet   Quantity: 1   Price: $16.00 (Ingredients: flour, sugar, cocoa powder, food coloring, eggs,  butter, baking soda, baking powder, salt) WeddingCake: 3-Layer/3-Tier – Vanilla   Quantity: 1   Price: $135.00(Ingredients: flour, sugar, buttermilk, coffee, eggs,  butter, baking soda, baking powder, salt)  —————————————Report for Auburn’s Best Bakery (by Flavor)————————————— Pie: Weekly Special – Apple   Quantity: 1   Price: $12.00 (Ingredients: flour, sugar, apple, cinnamon, butter,  baking soda, salt) Cake: Birthday – Chocolate   Quantity: 1   Price: $8.00 (Ingredients: flour, sugar, cocoa powder, vanilla, eggs,  butter, baking soda, baking powder, salt) Cookie: Chips Delight – Chocolate Chip   Quantity: 12   Price: $4.20 (Ingredients: flour, sugar, dark chocolate chips, butter, baking soda,  salt)Pie: Summer Special – Key Lime   Quantity: 1   Price: $14.00(Ingredients: flour, sugar, lime juice, lemon juice, graham crackers,  butter, baking soda, salt) Cake: 2-Layer – Red Velvet   Quantity: 1   Price: $16.00 (Ingredients: flour, sugar, cocoa powder, food coloring, eggs,  butter, baking soda, baking powder, salt) WeddingCake: 3-Layer/3-Tier – Vanilla   Quantity: 1   Price: $135.00(Ingredients: flour, sugar, buttermilk, coffee, eggs,  butter, baking soda, baking powder, salt) —————————————Excluded Records Report————————————— *** invalid category *** for line:D,Chips Delight,Chocolate Chip,12,flour,sugar,dark chocolate chips,butter,baking soda,salt*** invalid category *** for line:R,Weekly Special,Apple,1,0,flour,sugar,apple,cinnamon,butter,baking soda,salt—-jGRASP: operation complete.<strong> </strong></td>

  </tr>

 </tbody>

</table>

<table>

 <tbody>

  <tr>

   <td width="90"></td>

  </tr>

  <tr>

   <td></td>

   <td></td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<strong> </strong>