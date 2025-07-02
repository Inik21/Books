# Introduction

For who is this book useful:

- those looking to complete the **Java SE 21 Developer Professional exam (1Z0-830)**, commonly referred to as as the **OCP (Oracle Certified Professional) 21 exam**
- those looking to gain a deeper understanding and appreciation of Java

## Understanding the Exam

In this section, we discuss the details of the exam, along with some history of previous certification exams.

### Reviewing the Format of the Exam

The details of the exam are as follows:

- **Time limit:** 120 minutes
- **Number of questions:** 50
- **Passing score:** 68% (34 questions)

The exam consists entirely of multiple-choice questions. There are between four and ten possible answers. If a question has more than one answer, the question specifically states exactly how many correct answers there are.
This book does not do that. We say `Choose all that apply` to make the questions harder. This means the questions in this book are generally harder than those on the exam.

### Considering the Exam Objectives

Oracle provides a list of objectives to guide you on what to study for the exam. Each objective defines a list of subobjectives providing additional details about the objective.

### Non-Objective Objectives

Oracle has a habit of adding additional assumptions and requirements outside the scope of exam objectives. For the 1Z0-830, that includes the following two lists of items.

**Exam Assumptions**

- **Missing package and import statements**: If sample code does not include package or import statements and the question does not explicitly refer to these missing statements, then assume that all sample code is in the same package or that import statements exist to support them.
- **No file or directory path names for classes**: If a question does not state the file names or directory locations of classes, then assume one of the following, whichever will enable the code to compile and run:

  - All classes are in one file.
  - Each class is contained in a separate file, and all files are in one directory.

- **Unintended line breaks**: Sample code might have unintended line breaks. If you see a line of code that looks like it has wrapped and this creates a situation where the wrapping is significant (for example, a quoted `String` literal has wrapped), assume that the wrapping is an extension of the same line, and the line does not contain a hard carriage return that would cause a compilation failure.
- **Code fragments**: A code fragment is a small section of source code presented without its context. Assume that all necessary supporting code exists and that the supporting environment fully supports the correct compilation and execution of the code shown and its omitted environment.
- **Descriptive comments**: Take descriptive comments, such as “setters and getters go here,” at face value. Assume that correct code exists, compiles, and runs successfully to create the described effect.

**Exam Expectations**

- Understand the basics of Java Logging API.
- Use Annotations such as `@Override`, `@FunctionalInterface`, `@Deprecated`, `@SuppressWarnings`, and `@SafeVarargs`.
- Use generics, including wildcards.

### Reviewing Question Types

The following list of topics is meant to give you an idea of the types of questions and oddities that you might come across on the exam.

- **Word Problems**: A small percentage of questions on the exam do not involve reading code and are instead word problems. These questions are fast to solve. For example, you could get asked which statements are true about I/O.
- **Code Questions with Extra Information Provided**: Imagine the question includes a statement like “XMLParseException is a checked exception.” It’s fine if you don’t know what an XMLParseException is or what XML is, for that matter. (If you are wondering, it is a format for data.) This question is a gift. You know the statement is about exception handling.
- **Code Questions with Embedded Questions**: To answer some questions on the exam, you may have to answer two or three subquestions. For example, the question may contain two blank lines and ask you to choose the two answers that fill in each blank. In some cases, the two answer choices are not related, which means you’re really answering multiple questions, not just one.
- **Code Questions with Long Options**: The hardest questions on the exam have multiple lines of code in each option. For example, some of the questions have 6 possible options and up to 30 lines of code in each.
- **Code Questions with Made-Up or Incorrect Concepts**: In the context of a word problem, the exam may bring up a term or concept that does not make any sense, such as falsely saying a record extends another record. In other cases, the exam may use a keyword that does not exist in Java, like struct. For these, you just have to read carefully and recognize when the exam is using invalid terminology to try to trick you.
- **Questions That Are Really Out of Scope**: When introducing new questions, Oracle includes them as unscored questions at first. This allows the exam creators to see how real exam takers do without impacting your score. You will still receive the number of questions the exam lists. However, a few of them may not count. These unscored questions may contain out-of-scope material or even errors.
