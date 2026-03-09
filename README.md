# email-data-processing-automation

## Overview (English)

This project demonstrates an automated workflow that processes information received via email files, extracts structured data, enriches it using a reference dataset, and generates organized Excel reports.

The objective is to automate repetitive manual tasks and transform unstructured email content into structured datasets that can be used for reporting or analysis.

---

## Problem

In many operational environments, important information arrives via email. Extracting this information manually and organizing it into spreadsheets is time-consuming and prone to human error.

Typical manual workflow:

1. Open each email
2. Identify relevant fields
3. Copy the information into spreadsheets
4. Cross-reference the data with internal reference files
5. Organize the results for reporting

This process is repetitive and inefficient, and there is a risk of manual errors.

---

## Solution

A Python script was developed to automate this process.

The script:

1. Reads `.eml` email files from a local folder
2. Extracts key information from the email body such as:

   * client name
   * client code
   * record type
   * relevant dates when applicable
3. Handles different message formats depending on the record type
4. Extracts structured values from tables contained in the email body when necessary
5. Cross-references the extracted information with a reference dataset
6. Enriches the dataset with additional fields such as:

   * responsible person
   * department
   * client code validation
   * status
7. Generates Excel outputs including:

   * a **consolidated dataset containing all processed records**
   * **individual Excel files grouped by responsible person**

---

## Workflow

```id="workflow1"
Email files (.eml)
        ↓
Email processing
        ↓
Data extraction
        ↓
Record categorization
        ↓
Cross-reference with reference dataset
        ↓
Excel outputs
```

---

## Project Structure

```id="structure1"
email-data-processing-automation
│
├─ emails
│   ├─ email_type_A.eml
│   ├─ email_type_B.eml
│   └─ email_type_C.eml
│
├─ results
│   ├─ output_all.xlsx
│   ├─ output_1.xlsx
│   ├─ output_n.xlsx
│   └─ unmatched_emails.xlsx
│
├─ reference_dataset.xlsx
└─ extract_info.py
```

---

## Outputs

The script generates multiple outputs depending on the processing results:

* **output_all.xlsx**
  Consolidated dataset containing all processed records.

* **output_1.xlsx / output_n.xlsx**
  Excel files generated for each responsible person.

* **unmatched_emails.xlsx**
  Records that could not be matched with the reference dataset.

---

## Technologies Used

* Python
* Pandas
* Excel data processing

---

## Data Privacy

This repository is based on a real workflow scenario.
All datasets and email examples included here have been anonymized to remove any sensitive or confidential information.

---

# Procesamiento Automatizado de Información desde Emails

## Descripción (Español)

Este proyecto muestra un flujo automatizado que procesa información recibida por archivos de correo electrónico, extrae datos estructurados, los enriquece utilizando un dataset de referencia y genera informes organizados en Excel.

El objetivo es automatizar tareas manuales repetitivas y transformar contenido no estructurado de emails en datasets organizados que puedan utilizarse para análisis o reporting.

---

## Problema

En muchos entornos operativos, información relevante llega por correo electrónico. Extraer esta información manualmente y organizarla en hojas de cálculo requiere tiempo y puede generar errores humanos.

Flujo manual típico:

1. Abrir cada email
2. Identificar los campos relevantes
3. Copiar la información a hojas de cálculo
4. Cruzar los datos con archivos de referencia
5. Organizar los resultados para reporting

Este proceso es repetitivo, ineficiente y existe riesgo de errores manuales.

---

## Solución

Se desarrolló un script en Python para automatizar este proceso.

El script:

1. Lee archivos de email `.eml` almacenados localmente
2. Extrae información relevante del contenido del email, como:

   * nombre del cliente
   * código de cliente
   * tipo de registro
   * fechas relevantes cuando aplica
3. Maneja diferentes formatos de email según el tipo de registro
4. Extrae valores estructurados desde tablas presentes en el cuerpo del email cuando es necesario
5. Cruza la información extraída con un dataset de referencia
6. Enriquece los datos con información adicional como:

   * responsable
   * departamento
   * validación de código de cliente
   * estado
7. Genera salidas en Excel que incluyen:

   * un **dataset consolidado con todos los registros procesados**
   * **archivos Excel individuales agrupados por responsable**

---

## Tecnologías utilizadas

* Python
* Pandas
* Procesamiento de datos en Excel

---

## Privacidad de los datos

Este repositorio se basa en un flujo de trabajo real.
Todos los datasets y ejemplos incluidos han sido anonimizados para eliminar cualquier información sensible o confidencial.

---

**Autor**

Norma Tomás
Business + Tech → Solutions with real impact
