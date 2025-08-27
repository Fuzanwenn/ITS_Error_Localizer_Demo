# ITS_Error_Localizer_Demo

## Motivation
In Computer Science (CS) education, we face the challenge of increasing student enrollments over the past few years. Consequently, it has become increasingly difficult to provide high-quality and individualized learning support, particularly for novice students. Mirhosseini et al. recently conducted an interview study with CS instructors to identify their biggest pain points. Among other issues, they found that CS instructors struggle with limited or no Teaching Assistant (TA) support and the generally time-consuming task of providing student feedback and grading assignments. Thus, CS instructors would greatly benefit from automating tutoring activities to support TAs in their responsibilities.

## Development
Intelligent Tutoring System (ITS) for Programming and Algorithms Education is a fully automated tutoring system developed at the Trustworthy and Secure Software Lab of the National University of Singapore (NUS) that aims to provide on-time personalized feedback to students and grading support to tutors/instructors for programming assignments in Computer Science (CS) courses. It is a language-independent system that can be used with any programming language (e.g., Python, Java, C, etc.). It supports various essential functionalities, including syntax error fixing, logical error localization / repairing, and programming conceptual automated grading. Notably, the ITS is tightly coupled with the advanced Generative AI techniques (i.e. large language models) to provide high-level natural language feedback to students. The ITS has been used in CS1010S and CS2040S at NUS.


# its-errorlocalizer-template

## Overview
The error localization is the basis for a well-working repair strategy as it identifies one of its main ingredients, the potential *fix locations*. This project will give you the chance for an in-depth study of existing error localization techniques and to apply these approaches in the context of our intelligent tutoring system. This project requires to:

* Perform a literature study on error/fault localization to make yourself familiar with the different approaches and analysis-based techniques.
* Design and implement your approach, which can work on the CFG-based program structure. Crucial is that you do not only find divergences in the control flow between the reference program and the student's submission but also identify potential *fix locations*.
* Evaluate the techniques and determine the strengths and weaknesses of the chosen techniques.


## Entry Points

* This projects has a dependency to the interpreter. Please use the provided interpreter service implementation [InterpreterServiceImpl](./its-integration-services/src/main/java/sg/edu/nus/se/its/interpreter/InterpreterServiceImpl.java). You can use the interpreter to execute a program model object as illustrated in the test cases in [BasicTest.java](./its-errorlocalizer/src/test/java/sg/edu/nus/se/its/errorlocalizer/BasicTest.java).

* [sg.edu.nus.se.its.errorlocalizer.ErrorLocalizerImpl](./its-errorlocalizer/src/main/java/sg/edu/nus/se/its/errorlocalizer/ErrorLocalizerImpl.java)
```
/**
 * Implements the concrete error localizer based on CFG alignment, with the algorithm you choose.
 */
public class ErrorLocalizerImpl implements ErrorLocalizer {

  @Override
  public ErrorLocalisation localizeErrors(Program submittedProgram, Program referenceProgram,
      List<Input> inputs, StructuralMapping structuralMapping, VariableMapping variableMapping,
      Interpreter interpreter) {
    throw new NotImplementedException();
  }

}
```

* You can use `mvn clean compile test` to build and test your implementation.

## References
[Intelligent Tutoring System for Programming and Algorithms Education](https://nus-its.github.io/courses/cs3213/intro.html)
