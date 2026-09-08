### ***PROGRAM 9  :*** 



package selenium;



import java.time.Duration;

import org.openqa.selenium.By;

import org.openqa.selenium.WebDriver;

import org.openqa.selenium.WebElement;

import org.openqa.selenium.support.ui.ExpectedConditions;

import org.openqa.selenium.support.ui.WebDriverWait;

import org.openqa.selenium.chrome.ChromeDriver;

import org.openqa.selenium.edge.EdgeDriver;

import org.openqa.selenium.firefox.FirefoxDriver;



public class program9 {



&#x20;   public static WebElement getElement(WebDriver driver, String locatorType, String locatorValue) {



&#x20;       By by;



&#x20;       switch(locatorType.toLowerCase()) {



&#x20;           case "id":

&#x20;               by = By.id(locatorValue);

&#x20;               break;



&#x20;           case "name":

&#x20;               by = By.name(locatorValue);

&#x20;               break;



&#x20;           case "classname":

&#x20;               by = By.className(locatorValue);

&#x20;               break;



&#x20;           case "tagname":

&#x20;               by = By.tagName(locatorValue);

&#x20;               break;



&#x20;           case "linktext":

&#x20;               by = By.linkText(locatorValue);

&#x20;               break;



&#x20;           case "partiallinktext":

&#x20;               by = By.partialLinkText(locatorValue);

&#x20;               break;



&#x20;           case "css":

&#x20;           case "cssselector":

&#x20;               by = By.cssSelector(locatorValue);

&#x20;               break;



&#x20;           case "xpath":

&#x20;               by = By.xpath(locatorValue);

&#x20;               break;



&#x20;           default:

&#x20;               throw new IllegalArgumentException("Invalid Locator Type");

&#x20;       }



&#x20;       WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(10));



&#x20;       return wait.until(ExpectedConditions.visibilityOfElementLocated(by));

&#x20;   }

&#x20;   

&#x20;   public static void main(String\[] args) {



&#x20;       WebDriver driver = new ChromeDriver();

&#x20;       WebDriver driver1 = new EdgeDriver();

&#x20;       WebDriver driver2 = new ChromeDriver();



&#x20;       driver.manage().window().maximize();



&#x20;       driver.get("https://www.amazon.com");



&#x20;       WebElement searchBox = getElement(driver, "id", "twotabsearchtextbox");



&#x20;       System.out.println("WebElement Returned Successfully");

&#x20;       System.out.println("Tag Name : " + searchBox.getTagName());

&#x20;       System.out.println("Element ID : " + searchBox.getAttribute("id"));



&#x20;       searchBox.sendKeys("Laptop");



&#x20;       WebElement searchButton = getElement(driver, "id", "nav-search-submit-button");

&#x20;       searchButton.click();



&#x20;       driver.quit();

&#x20;   }

}



\---------------------------------------------------------------------------------------------------------------------------

### ***PROGRAM 10 :*** 



package selenium;



import java.time.Duration;



import org.openqa.selenium.By;

import org.openqa.selenium.WebDriver;

import org.openqa.selenium.WebElement;

import org.openqa.selenium.chrome.ChromeDriver;

import org.openqa.selenium.support.ui.ExpectedConditions;

import org.openqa.selenium.support.ui.WebDriverWait;



public class program10 {



&#x20;   // Method to handle all locators with Dynamic Wait

&#x20;   public static WebElement getElement(WebDriver driver, String locatorType, String locatorValue) {



&#x20;       By by = null;



&#x20;       switch(locatorType.toLowerCase()) {



&#x20;           case "id":

&#x20;               by = By.id(locatorValue);

&#x20;               break;



&#x20;           case "name":

&#x20;               by = By.name(locatorValue);

&#x20;               break;



&#x20;           case "classname":

&#x20;               by = By.className(locatorValue);

&#x20;               break;



&#x20;           case "tagname":

&#x20;               by = By.tagName(locatorValue);

&#x20;               break;



&#x20;           case "linktext":

&#x20;               by = By.linkText(locatorValue);

&#x20;               break;



&#x20;           case "partiallinktext":

&#x20;               by = By.partialLinkText(locatorValue);

&#x20;               break;



&#x20;           case "css":

&#x20;           case "cssselector":

&#x20;               by = By.cssSelector(locatorValue);

&#x20;               break;



&#x20;           case "xpath":

&#x20;               by = By.xpath(locatorValue);

&#x20;               break;



&#x20;           default:

&#x20;               throw new IllegalArgumentException("Invalid Locator Type");

&#x20;       }



&#x20;       WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(10));



&#x20;       return wait.until(ExpectedConditions.visibilityOfElementLocated(by));

&#x20;   }



&#x20;   public static void main(String\[] args) {



&#x20;       WebDriver driver = new ChromeDriver();



&#x20;       driver.manage().window().maximize();



&#x20;       driver.get("https://www.google.com");



&#x20;       WebElement searchBox = getElement(driver, "name", "q");



&#x20;       System.out.println("WebElement Returned Successfully");

&#x20;       System.out.println("Tag Name : " + searchBox.getTagName());



&#x20;       searchBox.sendKeys("Selenium");



&#x20;       driver.quit();

&#x20;   }

}



\---------------------------------------------------------------------------------------------------------------------------

### ***PROGRAM 11 :*** 



package selenium;



import org.openqa.selenium.WebDriver;

import org.openqa.selenium.firefox.FirefoxDriver;





public class program11 {



&#x09;public static void main(String\[] args) {

&#x09;	// TODO Auto-generated method stub

&#x09;	

&#x09;	 // Create Firefox WebDriver object

&#x20;       WebDriver driver = new FirefoxDriver();



&#x20;       // Open a website

&#x20;       driver.get("https://www.google.com");



&#x20;       // Print page title

&#x20;       System.out.println("Page Title: " + driver.getTitle());



&#x20;       // Close the browser

&#x20;       driver.quit();



&#x09;}



}





\---------------------------------------------------------------------------------------------------------------------------

### ***PROGRAM 12 :*** 



package selenium;



import org.openqa.selenium.WebDriver;

import org.openqa.selenium.chrome.ChromeDriver;



public class program12 {



&#x20;   public static void main(String\[] args) throws InterruptedException {



&#x20;       // Launch Chrome browser

&#x20;       WebDriver driver = new ChromeDriver();



&#x20;       // Open the website

&#x20;       driver.get("https://www.amazon.com");



&#x20;       // Display success message

&#x20;       System.out.println("Website is opened successfully");



&#x20;       // Wait for 5 seconds

&#x20;       Thread.sleep(5000);



&#x20;       // Close the browser

&#x20;       driver.quit();



&#x20;       System.out.println("Browser closed successfully");

&#x20;   }

}



\---------------------------------------------------------------------------------------------------------------------------

### ***PROGRAM 13 :*** 



package selenium;



import org.openqa.selenium.By;

import org.openqa.selenium.WebDriver;

import org.openqa.selenium.chrome.ChromeDriver;



public class program13 {



&#x20;   public static void main(String\[] args) {



&#x20;       // Launch Chrome

&#x20;       WebDriver driver = new ChromeDriver();



&#x20;       // Open file upload website

&#x20;       driver.get("https://the-internet.herokuapp.com/upload");



&#x20;       // Locate the file upload element and upload the file

&#x20;       driver.findElement(By.id("file-upload"))

&#x20;             .sendKeys("C:\\\\Users\\\\Manoj\\\\Desktop\\\\sample.txt");



&#x20;       // Click the Upload button

&#x20;       driver.findElement(By.id("file-submit")).click();



&#x20;       // Display success message

&#x20;       System.out.println("File uploaded successfully");



&#x20;       // Close the browser

&#x20;       driver.quit();

&#x20;   }

}



\---------------------------------------------------------------------------------------------------------------------------

### ***PROGRAM 14 :*** 



package selenium;



import org.openqa.selenium.By;

import org.openqa.selenium.WebDriver;

import org.openqa.selenium.chrome.ChromeDriver;



public class program14 {



&#x20;   public static void main(String\[] args) {



&#x20;       // Launch Chrome browser

&#x20;       WebDriver driver = new ChromeDriver();



&#x20;       // Open the website

&#x20;       driver.get("https://the-internet.herokuapp.com/");



&#x20;       // Access link using linkText()

&#x20;       driver.findElement(By.linkText("A/B Testing")).click();



&#x20;       // Go back to the previous page

&#x20;       driver.navigate().back();



&#x20;       // Access link using partialLinkText()

&#x20;       driver.findElement(By.partialLinkText("Form")).click();



&#x20;       // Close the browser

&#x20;       driver.quit();

&#x20;   }

}



\---------------------------------------------------------------------------------------------------------------------------

### ***PROGRAM 15 :*** 



package selenium;



import org.openqa.selenium.By;

import org.openqa.selenium.WebDriver;

import org.openqa.selenium.edge.EdgeDriver;

import org.openqa.selenium.support.ui.Select;



public class program15 {



&#x20;   public static void main(String\[] args) {



&#x20;       // Launch Edge browser

&#x20;       WebDriver driver = new EdgeDriver();



&#x20;       // Open the website

&#x20;       driver.get("https://www.selenium.dev/selenium/web/formPage.html");



&#x20;       // Locate the dropdown

&#x20;       Select dropdown = new Select(

&#x20;               driver.findElement(By.name("multi-select"))

&#x20;       );



&#x20;       // Select multiple items

&#x20;       dropdown.selectByVisibleText("Volvo");

&#x20;       dropdown.selectByVisibleText("Saab");



&#x20;       // Display success message

&#x20;       System.out.println("Multiple items selected successfully");



&#x20;       // Close browser

&#x20;       driver.quit();

&#x20;   }

}



\---------------------------------------------------------------------------------------------------------------------------

