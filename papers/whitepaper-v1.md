# Workforce Modelling for the Modern Web

## Introduction

**Workforce modeling** is the process by which the need for skilled workers (demand) is matched directly with the availability of skilled workers (supply). Electronic systems are integral in the workforce modelling process as it provides data to objectively analyze the mismatch and relevance of credentials.

In order for electronic systems to generate this actionable data, there needs to be standardized data models for the systems to communicate with each other. In addition, the functions of each of these systems must be clearly identified. 

An important need for machine-readable data is to allow for its direct consumption in Machine Learning and Artificial Intelligence technologies to create an AI Workforce Model. The model can be used to provide recommendations on what jobs are in demand and what duties are most important to organizations within an occupational area.

An optimally designed platform comprised of interconnected electronic systems and powered by AI can produce a highly effective and efficient workforce marketplace that will provide tremendous benefits to issuers, holders of credentials and organizations.

## Target Audience

The target group includes Organizations, Training Institutions and Industry Groups desirous of developing electronic systems for digital identities, credentials and job postings to improve the efficiency and effectiveness of workforce development strategies.

## Definitions

**Electronic System** – an application, usually a web, mobile or desktop application, used to store, process and output data.

**Digital Platform** – a collection of electronic systems that communicate with each other to achieve a common objective.

**Data Model** – a format, e.g. JSON or CSV, used to structure data for electronic systems to read (machine -readable) and communicate with each other.

**Holder** – the holder of a digital identity or digital credential, e.g.: worker.

**Worker** – a person that works for an organization.

**Organization** – a entity that employs workers.

**Issuer** – an entity that issues digital credentials.

**Digital Identity** – a machine readable identity of a holder or issuer.
W3C - The World Wide Web Consortium (W3C) develops standards and guidelines for the web.

**Decentralized Identifier (DID)** – a digital identity based on the W3C specification for digital identifiers.

**DID:JWK** – a decentralized identifier using the did:jwk method.

**DID:WEB** – a decentralized identifier using the did:web method.

**Asymmetric Key Pair** – A pair of private and public cryptographic keys controlled by issuers and holders and used to digitally sign data.

**Digital Credential** – a machine readable credential issued to a holder based on competences that they have demonstrated.

**Verifiable Credential (VC)** – a specification for the digital credential data model published by the W3C.

**Achievement Collection** – a machine readable collection of credentials achieved by a holder that is grouped within an occupational area.

**Offering Collection** – a machine readable collection of credentials offered by an issuer that is grouped within an occupational area.

**VC Wallet** – an electronic system for creating digital identities and storing digital credentials.

**VC Issuer** – an electronic system for the issuance of digital credentials.

**Workforce Hub** – an electronic system for posting job vacancies by organizations and for workers to respond to these postings.

**Standard Occupation Classification** – a standardized system to classify occupations.

**Job Posting** – a description of a job posted by an organization for recruiting purposes.

**Occupational Duties** -the tasks performed by workers in an occupational area.

**Machine Learning (ML)** – the process that an electronic system uses to perform statistical analysis of data to uncover trends and make predictions.

**Artificial Intelligence (AI)** – a technology that an electronic system uses to simulate human intelligence by utilizing various machine learning processes.

**Workforce AI Model** – is produced as a result of training using the data from the workforce data models. It is used to make predictions and recommendations to reduce the mismatch and improve the relevance of credentials.

**API (Application Programming Interface) Server** – a server that provides an HTTP REST interface for clients to access data or electronic services.

## What Problems Need to Be Solved

- Reducing the **mismatch** of workers supplied for perceived occupations and the occupations that organization are actually demanding.

- Improving the **relevance** of credentials that holders possess to the occupational duties actually required by the organizations.

## Objective

The objective is to define the data models for the electronic communication of digital identities, credentials and job postings. In addition, a design for a digital platform will be outlined identifying the various electronic systems communicating with these data models.	

## Deliverables

- **Defining data models** for: Digital Identity, Digital Credential and Digital Job Posting.

- **Defining the functions** of the electronic systems for: a VC Wallet, VC Issuer and Workforce Hub that comprise the digital platform.

- **Building prototypes** for: a VC Wallet API Server, VC Issuer API Server and Workforce Hub API Server 

## Digital Identity

A digital identity is a machine-readable unique identifier assigned to a holder or issuer. The owner of the identity has sole control over it. 
Digital identity shall conform to the specification for Decentralized Identifiers (DID) published by W3C. 

## Holder

### DID-JWK

Holders will be issued a digital identity that conforms to the DID-JWK  method. In this method, the DID resolves directly to a DID Document. The DID Document is a JSON file structure that identifies the public cryptographic key the holder controls. 

The DID is created in a VC Wallet and is designed to be portable. The DID will be provided as a string in a text file. The DID shall be downloadable and the text file can be stored in any storage system (e.g.: Hard Drive, Cloud Drive, Thumb Drive, etc.) 

**A VC Wallet shall not reveal or share a holder’s DID and the asymmetric cryptographic keys with any third-party individual, organization or electronic system.**

Example DID:JWK:

```
did:jwk:eyJlIjoiQVFBQiIsImt0eSI6IlJTQSIsIm4iOiI0N1x1MDAyQnBhZGcwXHUwMDJCbHY5NFdzd0c2d3dyeG14TVIzdGZlWWlQdkhpbkoyQnBEOGl0QXM0WktSUU1jL2ZGbDRzRHJpSkE3TkZXVW5QT2s0bThwUk5RcUV2bllMYmdXWDdoQWNmVmdOMUxHQ1lsTnNNOUNSUjdKWC9RWGl1L0s2eWpCR2ZHQzRtdGxzcEsvVGNkMTMyNDI5OHVQTWlQNlZlOGN0YnVla2U2M1JKbEpFcWt3OUVqbHhuUW1ja0U4RFhcdTAwMkJiNkFZdFFOVkF0QndvRGlna3VITFdyNGRpWUZPNE1DclEwbHFMMXRYOFBCQmkvSk0xL09cdTAwMkJhaVZUelVQZnMwNzlnWVx1MDAyQllvRk1oSzRWSy9vU0VDOFJsanJnVTQ3OTB1d3hjSWVtNkxJT1o2NGIzcG5KUHBFWGNhS09DaXFNZnlWcmk2Z1BoQ3k2Qmp1azBqQnBUNTJydnZkL3lRPT0ifQ
```

The public key identified in the DID is used to verify various cryptographic signatures produced by the holder. In this way, a verifier can verify that the signed data produced by a holder, in fact, originated from the holder.

Example public key:

```
-----BEGIN RSA PUBLIC KEY-----
MIIBCgKCAQEA47+padg0+lv94WswG6wwrxmxMR3tfeYiPvHinJ2BpD8itAs4ZKRQ
Mc/fFl4sDriJA7NFWUnPOk4m8pRNQqEvnYLbgWX7hAcfVgN1LGCYlNsM9CRR7JX/
QXiu/K6yjBGfGC4mtlspK/Tcd1324298uPMiP6Ve8ctbueke63RJlJEqkw9Ejlxn
QmckE8DX+b6AYtQNVAtBwoDigkuHLWr4diYFO4MCrQ0lqL1tX8PBBi/JM1/O+aiV
TzUPfs079gY+YoFMhK4VK/oSEC8RljrgU4790uwxcIem6LIOZ64b3pnJPpEXcaKO
CiqMfyVri6gPhCy6Bjuk0jBpT52rvvd/yQIDAQAB
-----END RSA PUBLIC KEY-----

```

Example of signed data in the form of a JSON Wed Token (JWT):

```
eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCJ9.eyJpdGVtIjoiaGVsbG8gd29ybGQifQ.qyk_Ax6KhvKUjSzho9zawhX4bwvcTRkOrm6f0zaEjLmZWLVuUIlPQ7EwmlqhYzgyIiV_V3-0K7GQCZ7vjeAOb42swRLagVjp9CRMwh3Z-01LFaovc_e00r2h1I9PNkDgJz3N7KgNII59gQisznFeuT3IfVZ8YymvSGblRhCWBN-84kbioZwWTNpd692e49pQ5z24ITe0dNG7CGYu_4jKdfhRrQg8q4BaEte-DG-kwAtb4OjvadD9R4Iak6mbMzR7sGgjVsF-GVXbgvSm_FDye3uhKjfIgV9N6Xq01e6KmY788yTSIYE9NFP_D9wYtgw98aasSjLFDmJErfgd_U8Y4A
```

This signed data will be verified that it originated from the holder by using the holder’s public key identified in the DID document.

The holder of the DID has a matching private key. The holder can create their public and private asymmetric cryptographic keys in the VC Wallet.  

The keys will be RS256 of size 2048 bits. The public and private keys will be in the form of a string in a text file. The holder will download and save their keys in their system of choice. 

**The holder should not share their private keys with anyone.** 

The private key is used by the holder to sign data. The holder’s public key is used to verify the holder’s signature.

Example private key:

```
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEA47+padg0+lv94WswG6wwrxmxMR3tfeYiPvHinJ2BpD8itAs4
ZKRQMc/fFl4sDriJA7NFWUnPOk4m8pRNQqEvnYLbgWX7hAcfVgN1LGCYlNsM9CRR
7JX/QXiu/K6yjBGfGC4mtlspK/Tcd1324298uPMiP6Ve8ctbueke63RJlJEqkw9E
jlxnQmckE8DX+b6AYtQNVAtBwoDigkuHLWr4diYFO4MCrQ0lqL1tX8PBBi/JM1/O
+aiVTzUPfs079gY+YoFMhK4VK/oSEC8RljrgU4790uwxcIem6LIOZ64b3pnJPpEX
caKOCiqMfyVri6gPhCy6Bjuk0jBpT52rvvd/yQIDAQABAoIBAFeA4DqGk3RNu/HM
GSPIuLvOB0Jz2TeyIB5HGWZLLfBJQbAjT3t7lkRNNc2GSS8uv5XoXxC7Rx+Dv3sc
d8LN41mFWYkSAdzsT6Hgmjh+tKEcuJFlEwTvbK9fCvySso8WhiXoNX+C7wKwhbRn
KeCgiS8WW2ZQx3XnSErZwsN8Xnjxw65luzgC5d0eD0TlsIjxj9DfCO+NvZjKyrBh
AN2R7KnuG9RDNwaBlvVOajcCw7dGI+EsZzbYDCVCb4g4MxyEcZ4cqc1ty7MK0YlO
zh5iDBikBYqsJTal4fKpEcNhx4ZPCoVACzikmwXlsIBa2qGsGUiViko1sMd0mbLi
+k/cUzECgYEA/3U8yVvwjFZVHk0kDcDoNvgrWYkBQST19iyAexpyESgUIyZxr0bb
5/LYTG4+2EXbMUbdQQGZ9gHQj5R1ff8CAw17mEcQM8M+le1Q/E3EWUnexBmwcfk5
quipFlpt4M2bZJ51GX2SYcssl94xu2wYlQz4/I9gxn/NL8ii1gb4zGcCgYEA5Dtf
dT3ommIWXrnAey3LgJPJA62HNHsiX4NX8kPTbSRmAXQJCXLfz3kVZ8/WN0JIr8MG
zOOHFrqEX+yKn56xIIGm1A/UXPKRjRfX3exEzpW0T4jSgJtYTssD1zAl47ZccqcT
+cxfrjvQDwA94BCGyUWPNkn/zfZDKs+axEjItE8CgYA6XRGnO38owOyvgJZVIhar
wGU/DoMf3A7p0F8GQROAgfSf1z+v+PNy+dObGrD2/nbGulcAbBo9z0pUE2oIgEN4
aRMsxkeYW+onnNGc4zOR5sOjb+8VCwi22HMRLVXfP3paMa21RjA0cZPdmqEoHdk7
7HvST/ufPkGlwiQZ2/vpzwKBgHToPNNvbNB34gGPoJr4MD+ic9sgbhth34+RVeFR
AOHtPRsNdvuSDjbWTTKp8Y7Iszbk7XzSJ4Zq8Be6sJ9myFBgWTZTDXK3BfuB9R9G
QVCYuo3rBfi+mhNyRntZvG7SILTSBJd2KqSzGrY0Z314ubIroVoruY6k0G8DfMGC
jtxdAoGAf7BjgUq9G9Nt/Cvco2Kcm+L7JBIqRr6QVpycpxK2pXsUSQeTO0r5icKn
4JFno0a6tsY5qwSZijeJmciNYh+yyWaNNBy35WhnxJNiRsSpPLsdtKzkWrBUasyq
8nc1l/a5I4Oiijtuaf+bVGisn81f7+HNh87Qy4nTUb6+yWw1QWU=
-----END RSA PRIVATE KEY-----
```

The data model for the digital identity is in JSON format and will conform to the W3C DID Document. 

The W3C specification for the data model for digital identifiers will describe the details of this data model.

Example data model for digital identity – W3C DID Document:

```json
{
    "@context": [
        "https://www.w3.org/ns/did/v2",
        "https://w3id.org/security/suites/jws-2020/v1"
    ],
    "id": "did:jwk:eyJlIjoiQVFBQi9In0",
    "verificationMethod": [
        {
            "id": "did:jwk:eyJleGIxUXks..T09In0#0",
            "type": "JsonWebKey2020",
            "controller": "did:jwk:eyJlIdTAwMk..g3UT09In0",
            "publicKeyJwk": {
                "e": "AQAB",
                "kty": "RSA",
                "n": "8AwUWwe7..HiHQh7Q=="
            }
        }
    ],
    "authentication": [
        "did:jwk:eyJlIjoSE9UwaL2czc..GlIUWg3UT09In0#0"
    ],
    "assertionMethod": [
        "did:jwk:eyJlIjoi09t..09In0#0"
    ]
}

```

The digital identity is provided to the holder as a DID:JWK. The DID:JWK will resolve to a DID Document.

Once the holder has a digital identity (DID:JWK), they will provide this identity to issuers to create their credentials. The DID will be included in the credential to specify that the credential was issued to the holder of the DID. 

The DID is interoperable and can be used by any electronic system issuing digital credentials to the holder. The DID is also portable, since it is a text file, and can be stored by the holder in any file storage system, either online or offline.

## Issuer

### DID:WEB

The digital identity for the issuer will conform to the DID:WEB  method. In this method, the issuer must have a website and own a domain that it controls. The issuer will use a VC Issuer electronic system to generate an asymmetric key pair. The key would be RSA with size 2048 bit.  A DID Document will contain the issuers public key as a JSON Web Key (JWK). 

Example DID:WEB DID Document :

```json
{
    "@context": [
        "https://www.w3.org/ns/did/v1",
        "https://w3id.org/security/suites/jws-2020/v1"
    ],
    "id": "did:web:example.com",
    "verificationMethod": [
        {
            "id": "did:web:example.com#key-1",
            "type": "JsonWebKey2020",
            "controller": "did:web:example.com",
            "publicKeyJwk": {
                "e": "AQAB",
                "kty": "RSA",
                "n": "47+padg0+lv94WDPp....BpT52rvvd/yQ=="
            }
        }
    ],
    "authentication": [
        "did:web:example.com#key-1"
    ],
    "assertionMethod": [
        "did:web:example.com#key-1"
    ]
}

```

The issuer will place the DID Document as a JSON file in the root of its website. The domain that hosts the file must match the domain that is identified in the ‘id’ of the DID Document.

The file must be accessed at the URL : https://<issuer-domain>/.well-known/did.json

A verifier will access the public key (JWK) from this file hosted on the issuer’s website to verity the signature of a digital credential created by the issuer.

The issuer must have a stable website and domain. If the website or domain becomes in-accessible, the signature on the digital credential would not be verifiable.

## Verifiable Credential

### Issuer

An issuer will issue a digital credential to a holder. The issuer may be an employer, individual, training institution, AI, electronic system or any other expert entity.

### Data Model

The data model for a digital credential will conform to the specification: Verifiable Credentials Data Model published by the W3C . The verifiable credential will be in the form of a JSON Web Token (JWT). The JWT will be in the compact serialized format and be saved as a string in a text file. The text file can be downloaded and saved by the holder in any online or offline storage of their choice. In this way, the digital credential is portable and can be exchanged with any compatible electronic system.

Example digital credential as a JWT:

```
eyJhbGciOiJFUzI1NiIsInR5cCI6IkpXVCJ9.eyJ2YyI6eyJAY29udGV4dCI6WyJodHRwczovL3
d3dy53My5vcmcvMjAxOC9jcmVkZW50aWFscy92MSIsImh0dHBzOi8vd3d3LnczLm9yZy8yMDE4L
2NyZWRlbnRpYWxzL2V4YW1wbGVzL3YxIl0sImlkIjoiaHR0cDovL2V4YW1wbGUuZWR1L2NyZWRl
bnRpYWxzLzM3MzIiLCJ0eXBlIjpbIlZlcmlmaWFibGVDcmVkZW50aWFsIiwiVW5pdmVyc2l0eUR
lZ3JlZUNyZWRlbnRpYWwiXSwiaXNzdWVyIjoiaHR0cHM6Ly9leGFtcGxlLmVkdS9pc3N1ZXJzLz
U2NTA0OSIsImlzc3VhbmNlRGF0ZSI6IjIwMTAtMDEtMDFUMDA6MDA6MDBaIiwiY3JlZGVudGlhb
FN1YmplY3QiOnsiaWQiOiJkaWQ6ZXhhbXBsZTplYmZlYjFmNzEyZWJjNmYxYzI3NmUxMmVjMjEi
LCJkZWdyZWUiOnsidHlwZSI6IkJhY2hlbG9yRGVncmVlIiwibmFtZSI6IkJhY2hlbG9yIG9mIFN
jaWVuY2UgYW5kIEFydHMifX19LCJpc3MiOiJodHRwczovL2V4YW1wbGUuZWR1L2lzc3VlcnMvNT
Y1MDQ5IiwibmJmIjoxMjYyMzA0MDAwLCJqdGkiOiJodHRwOi8vZXhhbXBsZS5lZHUvY3JlZGVud
GlhbHMvMzczMiIsInN1YiI6ImRpZDpleGFtcGxlOmViZmViMWY3MTJlYmM2ZjFjMjc2ZTEyZWMy
MSJ9.giMDNtWUgKbvWL4pteSpSkrh-lhgkhJUZ_gatHdRvEFs9_kB4G9neABvTuuQKfwERzi2KF
Qz3X0nzF-jrOO-5w

```

### JWT Header

The JWT header will comprise of the JWT type and the signing algorithm. The signing algorithm will be RS256 (2048-bit size).

```json
{
    "alg": "RS256",
    "typ": "JWT"
}

```

### JWT Payload

The JWT payload shall comply with the data model as shown below:

```json
{
    "vc": {
        "@context": [
            "https://www.w3.org/ns/credentials/v2"
        ],
        "id": "urn:uuid:0c07c1ce-57cb-41af-bef2-1b932b986873",
        "type": [
            "VerifiableCredential"
        ],
        "issuer": "did:web:example.com",
        "validFrom": "2010-01-01T00:00:00Z",
        "credentialSubject": {
            "id": "did:jwk:ebfeb1f712e..f1c276e12ec21",
            "achievement": {
                "name": "Writing Code With C#",
                "description": "Write basic code with C# ... and statements"
            }
        }
    },
    "iss": "did:web:example.com",
    "jti": "http://example.com/credentials/123",
    "sub": "did:jwk:ebfeb1f712e..f1c276e12ec21"
}

```

The data model is described in the W3C specification for verifiable credentials provided in the reference. A detailed description for the data model is provided in the specification.

This issuer of this credential is identified with a DID:WEB digital identity. The holder is identified with a DID:JWK. 

The ``iss`` (issuer), ``jti`` (id) and ``sub`` (subject) property values of the JWT are copied from the relevant  ``vc``  property values. The name and description of the credential is specified in the achievement object.

Dates shall be in the ISO 8601 basic format.

### JWT Signature

The JWT is signed with the issuer’s private key. 

```
2ee5j77NK0kalrPDmjmeFEbLe_7ooayp7eSTlfNUaoki0IG3l56GdiTlKnp
8-excMvagOPf3nHGkDqwEufps4A
```

The signature can be verified with the issuer’s public key that is provided in a DID Document hosted at the root of the issuer’s website.

## Offering Collection

Issuers will group credentials into a collection and assign the group to an occupational area. The Standard Occupation Code (SOC) and title shall be included in a collection.

Example of an offering collection :

```json
{
    "id" : "urn:uuid:1duu04885-t4679-44774g",
    "issuer": "did:web:example.com",
    "occupationCode": "15-1251.00",
    "occupationTitle": "Computer Programmers",
    "credentials": [
        {
            "id":"urn:uuid:3664885-4776-4663-4645",
            "name":"Programming with C#",
            "description": "Write basic code with C# using ... statements"
        },
        {
            "id":"urn:uuid:346625-3476-3453-9845",
            "name":"Develop Desktop Applications",
            "description": "Develop desktop applications with C#"
        }
    ]
}

```

## Holder

A digital credential is issued to a holder that demonstrates competence is a specific occupational area or in discreet occupational duties (Micro Credentials). The holder of the credential is uniquely identified with a digital identity (DID:JWK). The digital credential will reference the holder by his/her digital identity within the digital credential.

### Achievement Collection

A holder can create a collection of credentials within an occupational area. They can upload this collection to a Workforce Hub in response to job postings. They can also use an URL Link or Embed Code to display their collections to the public or on social media sites.

## Standard Occupational Classification

The Standard Occupation Classification (SOC) managed by ONET  will be used to classify occupations. Each occupation will have a code and a title.

## Job Posting

A job posting will be made by an organization with a Workforce Hub electronic system. The purpose of the job posting is to recruit suitable workers. The job posting should include the SOC that is relevant to the job. Job posting can also be formatted as JSON or CSV documents and uploaded into a Workforce Hub.

Example job posting JSON:

```json
{
    "id": "urn:uuid:675896-35547-76589756",
    "job": "Computer Programmer C#",
    "occupationCode": "15-1251.00",
    "occupationTitle": "Computer Programmers",
    "duties": ["Write, analyze, review, ..","Correct errors by mak.."],
    "education": ["Degree IT","MCSE"],
    "experience": ["5 years programming", "2 years supervisory"]
}

```

Example job posting CSV:

```
id,job,occupationCode,occupationTitle,duties,education,experience
urn:uuid:67589,Computer Programmer,15-1251.00,Computer Programmers,"Write, analyze, review;Correct errors","Degree IT;MCSE","5 years programming; 2 years supervisory"

```

In the CSV format, arrays, such as duties, education and experience are separated by semi-colons (;) and enclosed by quotations (“”).

## VC Wallet

A VC Wallet is an electronic system used by a holder to manage their digital identity and verifiable credentials. 

The main functions of a VC Wallet are:

- Allow holders to create their digital identity
- Allow holders to download and save their digital identity to their storage device of choice
- Allow holders to upload and save their digital credentials
- Allow holders to create achievement collections
- Allow holders to display achievement collections to the public
- Allow holders to download their achievement collections and save them to their storage media or upload to a Workforce Hub

**A VC Wallet shall not share a holder’s digital identity or cryptographic keys with any third party.**

## VC Issuer

A VC Issuer is an electronic system used by an issuer to issue digital credentials; and by a holder to receive digital credentials. 

The main functions of the VC Issuer are to:

- Allow issuers to create digital credentials
- Allow issuers to create offering collections
- Allow issuers to issue digital credentials to holders
- Allow holders to download digital credentials and save it to their storage of choice or upload it to a VC Wallet

## Workforce Hub

A Workforce Hub is an electronic system used by an organization to create job postings to recruit potential workers. Holders can upload their achievement collections in response to job postings. Issuers can review postings to gather data with a view of developing credentials to meet the market demand of the organization.

The main functions of the Workforce Hub are to:

- Allow organizations to create or upload job postings
- Allow holders to upload achievement collections and respond to job postings
- Allow issuers to view job postings

### Machine Learning and Artificial Intelligence

The Workforce Hub should implement machine learning algorithms and Artificial Intelligence (AI) to promote an efficient match between demand and supply of workers. The AI should recommend to issuers and holders what jobs are in the highest demand. It should also suggest the most important duties that organization require for an occupation. This information should drive issuers to develop more relevant credentials for the market. To achieve the effectiveness of the workforce modelling process the follow criteria should be met by the AI:

- Reduce the mismatch of what the organizations demand and what the issuers supply
- Ensure the relevance of credentials to the organization based on the duties that they require for an occupation

## API Servers

An API server will provide REST API interface to a VC Wallet, VC Issuer and Workforce Hub. There should be three API Servers for each electronic system. As a deliverable, three API servers will be built for use by public organizations, issuers and governments.




















