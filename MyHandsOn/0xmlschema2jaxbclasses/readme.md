# XML Schema to JAXB Classes

## JAXB tools and plugins

Não utilizamos ferramentas como schemagen ou xjc diretamente. Normalmente utilizamos plugins. 
Vamos utilizar um maven plugin.

1. Procure por maven jaxb plugin. O melhor, segundo o instrutor é o jvnet. A última versão na 
época do treinamento é o 0.14.

## XML Schema to JAXB Classes

1. Create the project
- Spring boot project (jaxbxjc - from xml schema to java objects)
- Crie um diretório abaixo de src\main: xsd.
- Copie três resources (exceto o pom) dessa aula (steps to generate stubs from XML Schema) para esse diretório.
- A partir do pom dos resources da aula, copie o maven plugin jvnet (todo o build) para o pom do projeto

2. Create the schemas

3. Use the JAXB Plugin

4. Generate the stubs and use them
- No eclipse o goal generate sources é automaticamente executado e os arquivos são gerados, em src\generated, conforme
especificado no plugin

## Customize generated code using binding file

O código java gerado pode ser customizado no arquivo xjb, referencido no maven plugin.

## Marshalling and Unmarshalling

### Unmarshall the stubs

1. Criar uma classe src\main\java\study.ws.soap.jaxb.JAXBDemo, com o método main.

2. No método main:

```
JAXBContext context = JAXBContext.newInstance(Patient.class); // catch JAXBException
Marshaller marshaller = context.createMarshaller();

Patient patient = new Patient();
```