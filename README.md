System.setProperty("webDriver.chrome.driver", "D:\\\\Selenium\\\\chromedriver-win64\\\\chromedriver-win64");
		ChromeDriver driver = new ChromeDriver();
		driver.get("https://demo.spreecommerce.org/");
		driver.manage().window().maximize();
		WebElement target = driver.findElement(By.xpath("//a[@class = \"nav-link main-nav-bar-item main-nav-bar-category-button dropdown-toggle\" and @href = \"/t/categories/women\"]"));
		Actions act = new Actions(driver);
		act.moveToElement(target).perform();
		act.click().perform();
		Thread.sleep(2000);
		WebElement t1 = driver.findElement(By.xpath("//div[@title = \"Asymetric Sweater With Wide Sleeves\"]"));
		act.moveToElement(t1).perform();
		act.click().perform();
		Thread.sleep(2000);
		driver.findElement(By.xpath("//button[@class = \"border-left-0  flex-grow-0 flex-shrink-0 py-0 px-3 quantity-select-increase\"]")).click();
		Thread.sleep(2000);
		driver.findElement(By.id("add-to-cart-button")).click();
		driver.findElement(By.linkText("View cart")).click();
