# Algorithms Responsibility in Healthcare Context

Algorithms are now ubiquitous in healthcare contexts. It's hard to find
any hospital without a so called Health Information System (HIS).
Furthermore, in the last decades, Artificial Intelligence (AI) algorithms
have shown there ability to treat large amount of data and overcome
clinicians in specific task (ex. detection of microscopique nodules).
This especially the case of neural networks.

However, the use of such algorithms in healthcare context raises
several ethical issues:

* **Responsibility issues**: in case of medical errors, due to the
use of an AI tool, who is responsible?
* **Transparency issues**: algorithms such as neural networks
can appears as "black-box" tools for patients and clinicians,
and then generate reject
* **Biaised decisions issues**: data-driven algorithms have
tendency to reproduce, and sometimes amplify, discrminations
* **Design-reality issues**: Clinical Decision Support Systems (CDSS),
based oon AI or not, can fail if they don't fit with clinicians
needs or working process

During this course we'll learn how to identify the ethical
issues raised by the use of AI-based HIS and how to overcome them.
To do so, students will by dispach in groups and work on a use case based on
problematics from emergency departments and will have to propose an AI-based
HIS adapted to this use case. Each group have to choose one, and one only,
use case.

*N.B:* Proposed use cases can hide sub-problems or problems connected
to these use case. Propositions that identify these hidden problems
and propose solutions are welcomed.

## USE CASE: Patient triage in emergency

A main problematic in emergency departments is patient triage.
Clinicians in these departments have to continously prioritize
patient over other depending on several variables.
This prioritization is crucial and a mistake can lead to
medical errors or death.

In this use case, you'll have to propose an AI-based HIS
able to prioritize patient, with a score between 1-10, according to
several variables.
A dataset and a Jupyter’s notebook are available
in the repertory *UC-patient-triage*.

### Getting started

First of all, you’ll need to install:

* [Python](https://www.python.org/downloads/)
* [Oracle JDK](https://www.oracle.com/java/technologies/downloads/) ([OpenJDK](https://openjdk.org/) should also works)
* on windows: [Visual CPP build tools](https://visualstudio.microsoft.com/fr/visual-cpp-build-tools/)

Then, to use the Jupyter’s notebook, you’ll need to
install the necessary dependencies.

To do so, use the command lines below:

```{bash}
python -m venv .venv
.venv/Scripts/activate
pip install numpy==1.24.3
pip install -r requirements.txt
```

Feel free to install any additionnal python library you need.

Once all the dependencies are installed, you can run the notebook
by using the command below:

```{bash}
jupyter notebook UC-patient-triage/UC_Patient_Triage.ipynb
```

### What is expected from students

A presentation on the design of an AI-based HIS
adapted to the chosen use case.

We essentially expect students to identify ethical issues linked
to the of AI algorithms in the proposed use case, and to propose
a concept of an AI-based that overcome these issues. Of course,
each choice is the design has to be justified.

No real software is asked, only concepts.

## Acknowledgments

Datasets proposed in this course are synthetic 
and do not reflect reality. Patients have been generated
with [Synthea](https://synthetichealth.github.io/synthea/)
throught the following command:

```{bash}
java -jar synthea-with-dependencies.jar -p 10000 -s 42 -cs 1312 --exporter.fhir.export false --exporter.hospital.fhir.export false --exporter.csv.export true --exporter.symptoms.csv.export true
```
