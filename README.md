plugins {
    id 'application'
    id 'java'
}

group 'com.example'
version '1.0-SNAPSHOT'

repositories {
    mavenCentral()
}

dependencies {
    testImplementation 'org.junit.jupiter:junit-jupiter-api:5.8.1'
    testRuntimeOnly 'org.junit.jupiter:junit-jupiter-engine:5.8.1'
    // https://mvnrepository.com/artifact/org.seleniumhq.selenium/selenium-java
    implementation 'org.seleniumhq.selenium:selenium-java:2.41.0'
    // https://mvnrepository.com/artifact/org.squashtest.tm/spock-test-dependencies
    // https://mvnrepository.com/artifact/org.testng/testng
    testImplementation 'org.testng:testng:7.4.0'

}
test {
    useJUnitPlatform()
}
test{
    useTestNG()
}
application{
    mainClass='com.example.Main'
}

jar{
    manifest{
        attributes 'Main-Class':'com.example.Main'
    }
}
