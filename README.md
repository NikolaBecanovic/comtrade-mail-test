# comtrade-mail-test
@Test

    public void comtradePlisaniMeda() throws InterruptedException {

        driver.get("https://www.ctshop.rs/customer/account/create");
        Thread.sleep(20000);
        JavascriptExecutor js = (JavascriptExecutor) driver;
        WebElement popUpButtonOne = (WebElement) js.executeScript("return document.querySelector('#popup-smart-root-35743').shadowRoot.querySelector('#PsCloseButton')");
        popUpButtonOne.click();
        WebElement popUpButton = (WebElement) js.executeScript("return document.querySelector('#popup-smart-root-35018').shadowRoot.querySelector('#PsCloseButton')");
        popUpButton.click();
        wdWait.until(ExpectedConditions.elementToBeClickable(By.xpath("//button[text() = 'Prihvatam']"))).click();
        Actions actions = new Actions(driver);
        actions.moveToElement(driver.findElement(By.cssSelector(".am-opener"))).perform();
        actions.moveToElement(driver.findElement(By.linkText("Bela tehnika"))).perform();
        actions.moveToElement(driver.findElement(By.linkText("Šporeti"))).perform();
        wdWait.until(ExpectedConditions.elementToBeClickable(By.linkText("Kombinovani šporeti"))).click();
        wdWait.until(ExpectedConditions.elementToBeClickable(By.xpath("//button[text() = 'Prihvatam']"))).click();
        wdWait.until(ExpectedConditions.elementToBeClickable(By.xpath("//label[text() = 'Gorenje']"))).click();
        wdWait.until(ExpectedConditions.elementToBeClickable(By.linkText("Gorenje K5111WG kombinovani šporet"))).click();
        wdWait.until(ExpectedConditions.presenceOfElementLocated(By.xpath("//p[4]/strong[text() = 'Bela']")));
        Assert.assertTrue(driver.findElement(By.xpath("//p[4]/strong[text() = 'Bela']")).isDisplayed());
        Assert.assertEquals(("Bela"),
                driver.findElement(By.xpath("//p[4]/strong[text() = 'Bela']")).getText());
        driver.navigate().back();
        wdWait.until(ExpectedConditions.elementToBeClickable(By.linkText("Poništi sve filtere"))).click();
        wdWait.until(ExpectedConditions.elementToBeClickable(By.xpath("//label[text() = 'Beko']"))).click();
        wdWait.until(ExpectedConditions.elementToBeClickable(By.linkText("Beko FSS54010DW kombinovani šporet"))).click();
        wdWait.until(ExpectedConditions.presenceOfElementLocated(By.xpath("//span[contains(text(), '28.422')]")));
        Assert.assertTrue(driver.findElement(By.xpath("//span[contains(text(), '28.422')]")).isDisplayed());
        Assert.assertNotEquals(("25.579"),
                driver.findElement(By.xpath("//span[contains(text(), '28.422')]")).getText());
        WebElement Element = driver.findElement(By.linkText("Ocene"));
        wdWait.until(ExpectedConditions.elementToBeClickable(By.linkText("Ocene"))).click();
        wdWait.until(ExpectedConditions.elementToBeClickable(By.linkText("Ocene"))).click();
        js.executeScript("window.scrollBy(0,1000)");
        wdWait.until(ExpectedConditions.presenceOfElementLocated(By.xpath("//*[contains(text(), 'EKONOMICAN')]")));
        Assert.assertTrue(driver.findElement(By.xpath("//*[contains(text(), 'EKONOMICAN')]")).isDisplayed());
        Assert.assertEquals(("EKONOMICAN"),
                driver.findElement(By.xpath("//*[contains(text(), 'EKONOMICAN')]")).getText());
        wdWait.until(ExpectedConditions.presenceOfElementLocated(By.xpath("//*[contains(text(), '(28.11.2018)')]")));
        Assert.assertTrue(driver.findElement(By.xpath("//*[contains(text(), '(28.11.2018)')]")).isDisplayed());
        Assert.assertEquals(("(28.11.2018)"),
                driver.findElement(By.xpath("//*[contains(text(), '(28.11.2018)')]")).getText());
        wdWait.until(ExpectedConditions.presenceOfElementLocated(By.xpath("//*[contains(text(), 'Odluka o kupovini ovog sporeta je izmedju ostalog doneta zbog nase velike potrosnje struje, sada nam plinske ringle u tome mnogo pomazu. Rerna je dovoljno velika i za gostinsko spremanje a gril koristim u kombinaciji sa konvencionalnim pecenjem. Ciscenje rerne je prava pesma obzirom da ima Steam Shine program. Sve u svemu PUN POGODAK!')]")));
        Assert.assertTrue(driver.findElement(By.xpath("//*[contains(text(), 'Odluka o kupovini ovog sporeta je izmedju ostalog doneta zbog nase velike potrosnje struje, sada nam plinske ringle u tome mnogo pomazu. Rerna je dovoljno velika i za gostinsko spremanje a gril koristim u kombinaciji sa konvencionalnim pecenjem. Ciscenje rerne je prava pesma obzirom da ima Steam Shine program. Sve u svemu PUN POGODAK!')]")).isDisplayed());
        Assert.assertEquals(("Odluka o kupovini ovog sporeta je izmedju ostalog doneta zbog nase velike potrosnje struje, sada nam plinske ringle u tome mnogo pomazu. Rerna je dovoljno velika i za gostinsko spremanje a gril koristim u kombinaciji sa konvencionalnim pecenjem. Ciscenje rerne je prava pesma obzirom da ima Steam Shine program. Sve u svemu PUN POGODAK!"),
                driver.findElement(By.xpath("//*[contains(text(), 'Odluka o kupovini ovog sporeta je izmedju ostalog doneta zbog nase velike potrosnje struje, sada nam plinske ringle u tome mnogo pomazu. Rerna je dovoljno velika i za gostinsko spremanje a gril koristim u kombinaciji sa konvencionalnim pecenjem. Ciscenje rerne je prava pesma obzirom da ima Steam Shine program. Sve u svemu PUN POGODAK!')]")).getText());
        wdWait.until(ExpectedConditions.presenceOfElementLocated(By.xpath(("//*[contains(text(), 'Zorica')]"))));
        Assert.assertTrue(driver.findElement(By.xpath("//*[contains(text(), 'Zorica')]")).isDisplayed());
        Assert.assertEquals(("Zorica"),
                driver.findElement(By.xpath("//*[contains(text(), 'Zorica')]")).getText());
    }
