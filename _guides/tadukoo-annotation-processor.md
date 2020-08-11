---
title: Tadukoo Annotation Processor Guide
blurb: How to make Annotation Processors using Tadukoo Annotation Processor
---
If you make an annotation processor, Tadukoo Annotation Processor (part of [Tadukoo Util](/projects/TadukooUtil.html)) will be helpful, providing the framework for the annotation processor.

Your project needs to have Tadukoo Annotation Processor as a dependency, and use it as an annotation processor. In Maven, this can be done with the following in your pom.xml file:

**Note**: The following properties may already be defined in your pom if you're working on a Tadukoo Engine project, but in case they're not:
- ${tadukoo.util.groupID} should be com.github.tadukoo.util
- ${tadukoo.util.annotationprocessor.artifactID} should be TadukooAnnotationProcessor
- ${tadukoo.util.annotationprocessor.version} should be the current version of Tadukoo Annotation Processor

```
<dependencies>
	<dependency>
		<groupId>${tadukoo.util.groupId}</groupId>
		<artifactId>${tadukoo.util.annotationprocessor.artifactID}</artifactId>
		<version>${tadukoo.util.annotationprocessor.version}</version>
	</dependency>
</dependencies>
<build>
	...
	<plugins>
		<plugin>
			<artifactId>maven-compiler-plugin</artifactId>
			<configuration>
				<annotationProcessorPaths>
					<annotationProcessorPath>
						<groupId>${tadukoo.util.groupId}</groupId>
						<artifactId>${tadukoo.util.annotationprocessor.artifactID}</artifactId>
						<version>${tadukoo.util.annotationprocessor.version}</version>
					</annotationProcessorPath>
				</annotationProcessorPaths>
			</configuration>
		</plugin>
	</plugins>
	...
</build>
```

Your annotation processor should have the @AnnotationProcessor annotation on it. This annotation will place the canonical class name of your annotation processor into the 
"META_INF/services/javax.annotation.processing.Processor" file of your project. Having it here defines it as an annotation processor, so that projects depending on yours can actually use 
your annotation processors. If your class doesn't appear in this list, Java won't know about it.

Your annotation processor should also extend AbstractAnnotationProcessor. At that point, all you need to do is define your constructor and override 
processElements(Set<? extends Element> elements) throws Throwable.

Your constructor should just call the super constructor, passing in a class object for the annotation you're processing, e.g.:

```
public MyAnnotationProcessor(){
	super(MyAnnotation.class);
}
```

Then when you override processElements, you're given whatever type of elements are dictated by your annotation, and you need to process them. By extending AbstractAnnotationProcessor, you're 
given access to AnnotationUtil (a protected field defined as annotationUtil), which provides access to methods and constants to make it easier to process your annotations.

To check out what AnnotationUtil can do for you, you can check out the [Javadoc for it](/docs/TadukooUtil/current/com/github/tadukoo/util/annotation/process/AnnotationUtil.html).
