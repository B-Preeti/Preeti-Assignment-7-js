Inheritance using function prototype

Base class : Company
Properties: name, location
Methods:hireEmployee,displayDetails
Subclass:SoftwareCompany and Manufacturing Company

1. Base Class: Company 
  (i) function Company(name,location):Constructor function for creating company  objects
  (ii)hire employee,displaydetails are methods to hire an employee and return a string with company details.

2.Subclass: Software company
 (i) Constructor for SoftwareCompany that also calls the Company constructor and initializes numDevelopers
 (ii)Object.create(Company.protype): Sets up inheritance for company
 (iii)SoftwareCompany.prototype.hireEmployee: Overwrites the hireEmployee method to specify it’s for developers.
 (iv)SoftwareCompany.prototype.displayDetails: Overwrites the displayDetails method to include the number of developers.

3.Subclass: Manufacturing company 
  (i)function ManufacturingCompany(name, location, numMachines): Constructor for ManufacturingCompany that also calls the Company constructor and initializes numMachine
  (ii)Object.create(Company.prototype): Sets up inheritance from Company
  (iii)SoftwareCompany.prototype.constructor = SoftwareCompany: Corrects the constructor property to refer to SoftwareCompany.
  (iv)SoftwareCompany.prototype.hireEmployee: Overwrites the hireEmployee method to specify it’s for developers.
  (v)SoftwareCompany.prototype.displayDetails: Overwrites the displayDetails method to include the number of developers.

4.Subclass:Manufacturing Company 
   (i)function ManufacturingCompany(name, location, numMachines): Constructor for ManufacturingCompany that also calls the Company constructor and initializes numMachines.
   (ii)ManufacturingCompany.prototype = Object.create(Company.prototype): Sets up inheritance from Company.
   (iii)  ManufacturingCompany.prototype.constructor = ManufacturingCompany: Corrects the constructor property to refer to ManufacturingCompany.
   (iv)ManufacturingCompany.prototype.hireEmployee: Overwrites the hireEmployee method to specify it’s for workers.
   (v)ManufacturingCompany.prototype.displayDetails: Overwrites the displayDetails method to include the number of machines

5.Create Instances
   (i) const softwareCompanies = [...]: Creates an array of SoftwareCompany instances.
   (ii)const manufacturingCompanies = [...]: Creates an array of ManufacturingCompany instances.

6.Display Details
  (i)const softwareCompaniesDiv = document.getElementById('softwareCompanies'): Selects the div element for software companies.
  (ii)softwareCompaniesDiv.innerHTML = '<h2>Software Companies</h2>': Adds a heading for software companies.
  (iii)softwareCompanies.forEach(company => { ... }): Iterates through each software company and adds their details to the div.
  (iv)const manufacturingCompaniesDiv = document.getElementById('manufacturingCompanies'): Selects the div element for manufacturing companies.
  (v)manufacturingCompaniesDiv.innerHTML = '<h2>Manufacturing Companies</h2>': Adds a heading for manufacturing companies.
  (vi)manufacturingCompanies.forEach(company => { ... }): Iterates through each manufacturing company and adds their details to the div.

7.Save the code 
8.Run the code
9.Find the details of software company and manufacturing company with name,location,number of developers.



 
   


   



