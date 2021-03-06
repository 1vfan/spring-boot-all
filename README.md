# spring-boot-all

- spring-boot-automatic-assembly
- spring-boot-dynamic-datasource
- spring-boot-extension-validator
- spring-boot-unified-response

## spring-boot-automatic-assembly

Auto Assembly to Configure EnableAutoConfiguration.class with custom Annotation.

- Use @Configuration or Create custom Annotation(@SpringDemoConfiguration).

- Implements ImportSelector to Create custom Annotation(@EnableDemoConfiguration).
 
- Implements Condition to Create custom Annotation(@ConditionalOnDemo).

- Use the above custom Annotation to Mark SpringDemoAutoConfiguration.

- Create custom META-INF/spring.factories and configure EnableAutoConfiguration.class.

## spring-boot-dynamic-datasource

Dynamic Route DataSource to Create SqlSessionFactory with custom Annotation.

- Configure Druid(or Hikari) for DataSource.

- Extends AbstractRoutingDataSource and Override determineCurrentLookupKey().

- Configure Mybatis to Create SqlSessionFactory.

- Create custom Annotation(@Dynamic) with DataSource key.

- Configure AOP to Intercept @Dynamic and set value to ThreadLocal.

- Use @Dynamic to mark @Service method.

## spring-boot-extension-validator

DIY Constraint Validator to Validate Request Parameter with custom Constraint Annotation.

- Extension MethodValidationPostProcessor to support fail_fast model.

- Create custom Annotation(@GeoLonCheck).

- Implements ConstraintValidator to Configure Validation logic.

- Use @NotNull and @GeoLonCheck to mark Field.

## spring-boot-unified-response

Unified Global ResponseBody for different Result with custom Exception.

- Create unified and global response Entity and Enum.

- Extends RuntimeException to Create Custom Exception.

- Use @ControllerAdvice and @ExceptionHandler to Intercept Exception.class.

- Assemble response Entity with different Exception Instance.

- Return success or error ResponseBody.