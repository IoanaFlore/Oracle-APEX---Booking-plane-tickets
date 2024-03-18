# Oracle-APEX---Booking-plane-tickets
## *Application Description*
#### Air transportation is a vital option for fast and efficient travel between different destinations. On the basis of a ticket, people can use air transport. The application aims to provide information to the user with reference to everything he needs for a flight by plane, thus the user will avoid congestion and lost time for purchasing a ticket at the counter. The database will provide details about both the companies and the flights available for purchasing tickets, as well as information about the prices offered.

## *Database design*

   **1. Logic diagram**

I created in Oracle SQL Developer Data Modeler the logical diagram for a database for booking plane tickets.

The figure below shows the logic diagram, which contains all the database entities for booking airline tickets and the links between them.

 ![image](https://github.com/IoanaFlore/Oracle-APEX---Booking-plane-tickets/assets/111995212/8da63e65-6fab-430d-91b0-0b518bcb2211)

 Business rules:

*  ORAS-AEROPORT CONNECTTION 1:M: A city can have one or more airports, and an airport must belong to a single city;
*  AIEROPORT-ZBOR CONNECTION 1:M: an airport can have one or more flights, and a flight must depart from only one airport;
*  AEROPORT-ZBOR1 CONNECTION 1:M: an airport can have one or more flights, and a flight must depart from only one airport;
*  COMPANIE-ZBOR CONNECTION 1:M: a company can have one or more flights, and a flight must belong to a company;
*  ZBOR-BILET CONNECTION 1:M: a flight may have one or more tickets for sale, and a ticket must belong to a single flight;
*  CLIENTI-BILET CONNECTION 1:M: A customer can own one or more tickets, and a ticket must belong to only one customer.



   **2. Relational diagram**

The figure below shows the relational diagram that forms the basis for the last stage of creating the database
physical data and is derived from the logic diagram. This diagram includes all relationships between entities and
attributes for which aliases were used.

 ![image](https://github.com/IoanaFlore/Oracle-APEX---Booking-plane-tickets/assets/111995212/1c98d2e3-e2b2-4a88-b742-df6ccc9e0111)



  **3. Generated SQL DDL script**

The generated SQL DDL script is at the link: 


   **4. Database generation in Oracle APEX based on SQL script**

  ![image](https://github.com/IoanaFlore/Oracle-APEX---Booking-plane-tickets/assets/111995212/7a382f9f-79df-4627-9fbd-91a227c4c871)
  
## *Application development*
The application was developed using Oracle Application Express. To access the app's functionality, users are required to log in via a login page. This login page is your first interaction with the app and includes the name of the app along with a suggestive logo.

![image](https://github.com/IoanaFlore/Oracle-APEX---Booking-plane-tickets/assets/111995212/8c9e38ac-671a-4b88-8dbd-3a9b6a468925)


   1. Home page

    
The first step in the development of the application involved the development of the main pages, including the secondary ones in the menu. In addition, each page is endowed with a distinctive symbol, reflecting the associated content. The home page is the main page itself, where a suggestive image illustrating the chosen theme is integrated

![image](https://github.com/IoanaFlore/Oracle-APEX---Booking-plane-tickets/assets/111995212/eb24c6ef-c48d-4f0f-996e-a522d0283b75)


   2. Forms page

Pagina principală Formulare conține alte 5 formulare secundare, după cum urmează:
*Formular oraș: contine un formular cu campurile necesare pentru a introduce orasul de unde calatorul va dori sa zboare cu avionul. Pentru ID_Oras a fost create un trigger pentru generare automata.
