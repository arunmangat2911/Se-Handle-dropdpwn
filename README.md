# Se-Handle-dropdpwn

package SeleniumSession;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.support.ui.Select;

public class handleDropDown {

	public static void main(String[] args) {

		System.setProperty("webdriver.chrome.driver", "C:\\Users\\Arun\\eclipse-workspace\\Selenium\\lib\\chromedrivers\\chromedriver.exe");
		WebDriver driver = new  ChromeDriver();
		
		driver.get("https://www.ebay.com/");
		
		Select select = new Select(driver.findElement(By.xpath("//*[@id=\"gh-cat\"]")));	
		select.selectByVisibleText("Books");
		
		driver.findElement(By.xpath("//*[@id=\"gh-btn\"]")).click();
		
	}

}
