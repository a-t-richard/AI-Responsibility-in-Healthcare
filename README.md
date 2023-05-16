# Algorithms Responsibility in Healthcare Context

Algorithms are now ubiquitous in healthcare contexts. It's hard to find
any hospital without a so-called Health Information System (HIS).
Furthermore, in the last decades, Artificial Intelligence (AI) algorithms
have shown their ability to treat a large amount of data and to overcome
clinicians in specific tasks (ex. detection of microscopic nodules).
This is especially the case with neural networks.

However, the use of such algorithms in healthcare contexts raises
several ethical issues:

* **Responsibility issues**: in case of medical errors, due to the
use of an AI tool, who is responsible?
* **Transparency issues**: algorithms such as neural networks
can appear as "black-box" tools for patients and clinicians,
and then generate a reject
* **Biaised decisions issues**: data-driven algorithms tend to reproduce,
and sometimes amplify, discriminations
* **Design-reality issues**: Clinical Decision Support Systems (CDSS),
based on AI or not, can fail if they don't fit with clinicians’
needs or working process

During this course, we'll learn how to identify the ethical
issues raised by the use of AI-based HIS and how to overcome them.
To do so, students will be dispatched in groups, work on a use case based on
problems from emergency departments, and will have to propose an AI-based
HIS adapted to this use case.

*N.B:* The proposed use case can hide sub-problems or problems connected
to this use case. Propositions that identify these hidden problems
and propose solutions are welcomed.

## USE CASE: Patient triage in emergency

One main problem in emergency departments is patient triage.
Clinicians in these departments have to continuously prioritize
patients over others depending on several variables.
This prioritization is crucial and a mistake can lead to
medical errors or death.

In this use case, you'll have to propose an AI-based HIS
able to prioritize patients, with a score between 1-10, according to
several variables.
A dataset and a Jupyter’s notebook are available
in the repertory *UC-patient-triage*.

### Getting started

First of all, you’ll need to install:

* [Python 3.9](https://www.python.org/downloads/release/python-3913/)
* [Oracle JDK](https://www.oracle.com/java/technologies/downloads/) ([OpenJDK](https://openjdk.org/) should also works)
* on windows: [Microsoft Visual C++ 14.0](https://visualstudio.microsoft.com/fr/visual-cpp-build-tools/)

Then, to use Jupyter’s notebook, you’ll need to
install the necessary Python libraries.

To do so, use the command lines below:

```{bash}
python -m venv .venv
.venv/Scripts/activate
pip install numpy==1.24.3
pip install -r requirements.txt
```

Feel free to install any additional python library you need.

Once all the dependencies are installed, you can run the notebook
by using the command below:

```{bash}
jupyter notebook UC-patient-triage/UC_Patient_Triage.ipynb
```

### What is expected from students

A presentation on the design of an AI-based HIS
adapted to the chosen use case.

We essentially expect students to identify ethical issues linked
to the use of AI algorithms in the proposed use case, and to propose
a concept of an AI-based HIS that overcome these issues. Of course,
each choice of design has to be justified.

No real software is asked, only concepts.

## Acknowledgments

The datasets proposed in this course are synthetic 
and do not reflect reality. Patients have been generated
with [Synthea](https://synthetichealth.github.io/synthea/)
through the following command:

```{bash}
java -jar synthea-with-dependencies.jar -p 10000 -s 42 -cs 1312 --exporter.fhir.export false --exporter.hospital.fhir.export false --exporter.csv.export true --exporter.symptoms.csv.export true
```
