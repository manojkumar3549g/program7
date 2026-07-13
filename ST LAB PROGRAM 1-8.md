PROGRAM 1 :





package selenium;

import org.openqa.selenium.WebDriver;

import org.openqa.selenium.chrome.ChromeDriver;



public class program1 {



&#x09;public static void main(String\[] args) {

&#x09;	// TODO Auto-generated method stub

&#x09;	WebDriver driver = new ChromeDriver();







&#x20;       // Open google.com



&#x20;       driver.get("https://www.google.com");







&#x20;       // Verify Title



&#x20;       String Title = driver.getTitle();



&#x20;       if (Title.contains("google")) {



&#x20;           System.out.println("Title Verification Passed");

&#x20;       } else {

&#x20;           System.out.println("Title Verification Failed");

&#x20;       }

&#x20;       // Verify URL Redirection

&#x20;       String currentUrl = driver.getCurrentUrl();

&#x20;       if (currentUrl.contains("google.com")) {

&#x20;           System.out.println("Redirected to google.com - Passed");

&#x20;       } else {

&#x20;           System.out.println("Redirected URL: " + currentUrl);

&#x20;           System.out.println("Redirection Verification Failed");

&#x20;       }



&#x20;       // Close Browser



&#x20;       driver.quit();



&#x09;}



}


--------------------------------------------------------------------------------------------------------------------------


PROGRAM 2 :







package selenium;

import org.openqa.selenium.WebDriver;

import org.openqa.selenium.chrome.ChromeDriver;



public class program2 {



&#x09;public static void main(String\[] args) {



&#x09;	

&#x09;			// Launch Chrome Browser

&#x09;	        WebDriver driver = new ChromeDriver();



&#x09;	        // Open Google India

&#x09;	        driver.get("https://www.google.com");



&#x09;	        // Print the page title

&#x09;	        System.out.println(driver.getTitle() + " opened successfully");



&#x09;	        // Close the browser

&#x09;	        driver.quit();





&#x09;}



}



\--------------------------------------------------------------------------------------------------------------------------



PROGRAM 3 :





package selenium;

import org.openqa.selenium.WebDriver;

import org.openqa.selenium.edge.EdgeDriver;

public class program3 {



&#x09;public static void main(String\[] args) {

&#x09;	// TODO Auto-generated method stub

&#x09;	// Create Edge browser instance

&#x20;       WebDriver driver = new EdgeDriver();



&#x20;       // Open Google

&#x20;       driver.get("https://www.gmail.com");



&#x20;       // Maximize window

&#x20;       driver.manage().window().maximize();



&#x20;       // Print page title

&#x20;       System.out.println("Title: " + driver.getTitle());



&#x20;       // Close browser

&#x20;       // driver.quit();et("https://www.google.com");



&#x20;       System.out.println("Title: " + driver.getTitle());



&#x20;       driver.quit();



&#x09;}



}





\--------------------------------------------------------------------------------------------------------------------------



PROGRAM 4 :





package selenium;

import org.openqa.selenium.WebDriver;

import org.openqa.selenium.chrome.ChromeDriver;

import org.openqa.selenium.edge.EdgeDriver;



public class program4 {



&#x09;public static void main(String\[] args) {

&#x09;	// TODO Auto-generated method stub

&#x09;	



&#x09;	WebDriver driver = new ChromeDriver();   

&#x20;        driver = new ChromeDriver();   

&#x20;       // Open website

&#x20;       driver.get("https://www.google.com");

&#x20;       // Print title

&#x20;       System.out.println("Page Title: " + driver.getTitle());

&#x20;       System.out.println("Chrome Opened Successfully");

&#x20;    // Close browser

&#x20;       driver.quit();

&#x20;       

&#x20;       

&#x20;       WebDriver driver1 = new EdgeDriver();

&#x20;       driver1.get("https://www.google.com");



&#x20;       // Maximize window

&#x20;       driver1.manage().window().maximize();



&#x20;       // Print page title

&#x20;       System.out.println("Title: " + driver1.getTitle());

&#x20;       System.out.println("Edge Opened Successfully");

&#x20;       driver1.quit();



&#x09;}



}





\--------------------------------------------------------------------------------------------------------------------------



PROGRAM 5 :





package selenium;

import java.util.List;

import java.util.Scanner;



import org.openqa.selenium.By;

import org.openqa.selenium.WebDriver;

import org.openqa.selenium.WebElement;

import org.openqa.selenium.chrome.ChromeDriver;

import org.openqa.selenium.support.ui.Select;

public class program5 {



&#x09;public static void main(String\[] args) {

&#x09;	// Get input from user

&#x20;       Scanner sc = new Scanner(System.in);

&#x20;       System.out.print("Enter the option to search: ");

&#x20;       String searchItem = sc.nextLine();



&#x20;       // Launch Chrome

&#x20;       WebDriver driver = new ChromeDriver();



&#x20;       // Open DemoQA webpage

&#x20;       driver.get("https://demoqa.com/select-menu");

&#x20;       driver.manage().window().maximize();



&#x20;       // Locate the Old Style Select Menu

&#x20;       WebElement dropdown = driver.findElement(By.id("oldSelectMenu"));



&#x20;       // Create Select object

&#x20;       Select select = new Select(dropdown);



&#x20;       // Get all options

&#x20;       List<WebElement> options = select.getOptions();



&#x20;       boolean found = false;



&#x20;       // Search the option

&#x20;       for (int i = 0; i < options.size(); i++) {



&#x20;           String text = options.get(i).getText();



&#x20;           if (text.equalsIgnoreCase(searchItem)) {



&#x20;               System.out.println(searchItem + " is present in the list box.");

&#x20;               System.out.println("Position of the element: " + (i + 1));



&#x20;               // Select the option

&#x20;               select.selectByVisibleText(text);



&#x20;               found = true;

&#x20;               break;

&#x20;           }

&#x20;       }



&#x20;       if (!found) {

&#x20;           System.out.println(searchItem + " is NOT present in the list box.");

&#x20;       }



&#x20;       sc.close();

&#x20;       driver.quit();

&#x09;}



}



\--------------------------------------------------------------------------------------------------------------------------



PROGRAM 6 :





package selenium;

import java.util.ArrayList;

import java.util.Collections;

import java.util.List;



import org.openqa.selenium.By;

import org.openqa.selenium.WebDriver;

import org.openqa.selenium.WebElement;

import org.openqa.selenium.chrome.ChromeDriver;

import org.openqa.selenium.support.ui.Select;



public class program6 {



&#x09;public static void main(String\[] args) {

&#x09;	// TODO Auto-generated method stub

&#x09;	 // Launch Chrome

&#x20;       WebDriver driver = new ChromeDriver();



&#x20;       // Open DemoQA Select Menu page

&#x20;       driver.get("https://demoqa.com/select-menu");

&#x20;       driver.manage().window().maximize();



&#x20;       // Locate the Old Style Select Menu

&#x20;       WebElement dropdown = driver.findElement(By.id("oldSelectMenu"));



&#x20;       // Create Select object

&#x20;       Select select = new Select(dropdown);



&#x20;       // Get all options

&#x20;       List<WebElement> options = select.getOptions();



&#x20;       // Store option text in ArrayList

&#x20;       ArrayList<String> colors = new ArrayList<>();



&#x20;       for (WebElement option : options) {

&#x20;           colors.add(option.getText());

&#x20;       }



&#x20;       // Sort the list

&#x20;       Collections.sort(colors);



&#x20;       // Print sorted options

&#x20;       System.out.println("Contents of the list in sorted order:");



&#x20;       for (String color : colors) {

&#x20;           System.out.println(color);

&#x20;       }



&#x20;       // Close browser

&#x20;       driver.quit();



&#x09;}



}





\--------------------------------------------------------------------------------------------------------------------------



PROGRAM 7 :





package selenium;



import java.util.HashSet;

import java.util.List;



import org.openqa.selenium.By;

import org.openqa.selenium.WebDriver;

import org.openqa.selenium.WebElement;

import org.openqa.selenium.chrome.ChromeDriver;

import org.openqa.selenium.support.ui.Select;



public class program7 {



&#x20;   public static void main(String\[] args) throws InterruptedException {

&#x20;   	

&#x20;   	// Launch Chrome Browser

&#x20;       WebDriver driver = new ChromeDriver();



&#x20;       // Open the webpage

&#x20;       driver.get("https://manojkumar3549g.github.io/duplicate-dropdown/");

&#x20;       driver.manage().window().maximize();



&#x20;       // Locate the dropdown

&#x20;       WebElement dropdown = driver.findElement(By.id("country"));



&#x20;       // Create Select object

&#x20;       Select select = new Select(dropdown);



&#x20;       // Get all options

&#x20;       List<WebElement> options = select.getOptions();



&#x20;       // Create HashSet to store unique options

&#x20;       HashSet<String> uniqueOptions = new HashSet<>();



&#x20;       // Add options to HashSet

&#x20;       for (WebElement option : options) {

&#x20;           uniqueOptions.add(option.getText());

&#x20;       }



&#x20;       // Print unique options

&#x20;       System.out.println("Unique Options in the List Box:");



&#x20;       for (String option : uniqueOptions) {

&#x20;           System.out.println(option);

&#x20;       }



&#x20;       // Close browser

&#x20;       driver.quit();



&#x20;       

&#x20;   }

}





\--------------------------------------------------------------------------------------------------------------------------



PROGRAM 8 :





package selenium;



import java.util.Set;



import org.openqa.selenium.WebDriver;

import org.openqa.selenium.chrome.ChromeDriver;

public class program8 {



&#x09;public static void main(String\[] args) {

&#x09;	// TODO Auto-generated method stub

&#x09;	

&#x09;	// Launch browser

&#x20;       WebDriver driver = new ChromeDriver();



&#x20;       // Open first website

&#x20;       driver.get("https://www.google.com");



&#x20;       // Open second window

&#x20;       driver.switchTo().newWindow(org.openqa.selenium.WindowType.WINDOW);

&#x20;       driver.get("https://www.amazon.in");



&#x20;       // Open third window

&#x20;       driver.switchTo().newWindow(org.openqa.selenium.WindowType.WINDOW);

&#x20;       driver.get("https://www.flipkart.com");



&#x20;       // Get all window handles

&#x20;       Set<String> windows = driver.getWindowHandles();



&#x20;       // Close each browser window

&#x20;       for (String window : windows) {

&#x20;           driver.switchTo().window(window);

&#x20;           driver.close();

&#x20;       }



&#x09;}



}







\--------------------------------------------------------------------------------------------------------------------------



