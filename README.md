### mapstruct
---
https://github.com/mapstruct/mapstruct

```java
@Mapper
public interface CarMapper {
  CarMapper INSTANCE = Mappers.getMapper( CarMapper.class );
  
  @Mapping(source = "numberOfSeats", target = "seatCount")
  CarDto carToCarDto(Car car);
}


plugins {
  id 'net.ltgt.apt' version '0.15'
}

apply plugin: 'net.ltgt.app-idea'
apply plugin: 'net.ltgt.apt-eclipse'

dependencies {
  compile 'org.mapstruct:mapstruct:1.3.0.Final'
  
  annotationProcessor 'org.mapstruct:mapstruct-processor:1.3.0.Final'
  testAnnotationProcessor 'org.mapstruct:mapstruct-processor:1.3.0.Final'
}

```

```sh
mvn clean install
mvn clean install -DskipDistribution=true
```

```
```


