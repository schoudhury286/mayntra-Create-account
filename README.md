helpwanted # mayntra-Create-account
I am unable to process the below codes in selenium using TestNg to select product to view product detail page and then do add to cart and then create new account to sign in. Please help

package Myntra.com;

import org.testng.annotations.Test;
import org.testng.annotations.BeforeMethod;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.support.ui.Sleeper;
import org.testng.annotations.AfterMethod;

public class Myntralink {

	   @Test
  public void mainLink() {
		   WebDriver driver = new ChromeDriver();
			 driver.get("https://www.myntra.com");
	  
	  WebElement Tab = driver.findElement(By.linkText("Women"));
	  Tab.click();
	  WebElement SubTab = driver.findElement(By.linkText("Kurtis & Tunics"));
	  SubTab.click();
	  WebElement product = driver.findElement(By.className("product-thumb"));
	  product.click();
	  //driver.findElement(By.className("size-buttons-unified-size")).click();
	 // driver.findElement(By.xpath("//input[’@class=pdp-add-to-bag pdp-button pdp-flex pdp-center’]"));
	  driver.findElement(By.linkText("Login")).click();
	  WebElement CreateAccount = driver.findElement(By.className("login-create-account-link login-link"));
	  CreateAccount.click();
	   //driver.findElement(By.id("gPlusLogin")).click();
	   //WebElement usserid = driver.findElement(By.id("identifierId"));
	   //usserid.sendKeys("abcd@mail.com");
	   //driver.findElement(By.linkText("Next")).click();
	  //WebElement password = driver.findElement(By.className("whsOnd zHQkBf"));
	  //password.sendKeys("Vegas123#");
	  //driver.findElement(By.linkText("Next")).click();
	  driver.findElement(By.xpath("//input[@name=’email’ and @class=’register-user-input-email register-user-input’]")).sendKeys("schoudhury286@gmail.com");
	  driver.findElement(By.xpath("//input[@name=’password’ and @class=’register-user-input-password register-user-input’]")).sendKeys("Vegas123#");
	  driver.findElement(By.xpath("//input[@name=’mobile’ and @class=’register-user-input-mobile register-user-input’]")).sendKeys("7411295669");

	  driver.findElement(By.xpath("//input[@value=’F’ and @class=’register-gender-radio’]")).isSelected();
	  driver.findElement(By.linkText("REGISTER")).click();
	  
	  
	  
     driver.close();
	  
  }

}
