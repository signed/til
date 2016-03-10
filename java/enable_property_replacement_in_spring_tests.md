# enable property replacement in @Value annotations in spring tests

Define a `PropertySourcesPlaceholderConfigurer` bean in your tests configuration.
The bean needs to be static to be able to do its job as a `BeanFactoryPostProcessor` and replace the property expressions after bean creation.
```java
@Configuration
public class TestConfiguration {

    @Bean
    public static PropertySourcesPlaceholderConfigurer properties() throws Exception {
        final PropertySourcesPlaceholderConfigurer pspc = new PropertySourcesPlaceholderConfigurer();
        Properties properties = new Properties();
        properties.setProperty("someProperty", "testValue");
        pspc.setProperties(properties);
        return pspc;
    }
}
```

To reuse an existing .properties file annotate the test configuration class with `@PropertySource("classpath:/com/myco/app.properties")` and point to the property file.