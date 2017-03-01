### _**Java and Selenium Samples Below**_

```Java
@RunWith(Parameterized.class)
public class JobSearchUsingGoogleTest {
	private static String baseUrl = "http://www.google.com";
	private String preferredJobSearchSite;
	private String jobTitle = "Software Tester";
	private static WebDriver driver;
	private static ScreenshotHelper screenshotHelper;
	
	public JobSearchUsingGoogleTest(String preferredJobSearchSite){
		this.preferredJobSearchSite = preferredJobSearchSite;
	}
		 
	@Parameters
	public static Collection<Object[] > data(){
		Object[][] data = new Object[][] {{"Indeed"}, {"Zip"}, {"fakesite"}};
		return Arrays.asList(data);
	}
  
	@Before
	public void openBrowser() {
	    driver = new ChromeDriver();
	    driver.get(baseUrl);
	    screenshotHelper = new ScreenshotHelper();
	    searchGoogle();
	}
...
```

[Java and Selenium WebDriver testing sample](https://github.com/mmccallister00/jobsearchtest)




[Go to my LinkedIn page](https://www.linkedin.com/in/mikemccallister)
