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

The generated SQL DDL script is at the link: [scrit](https://github.com/IoanaFlore/Oracle-APEX---Booking-plane-tickets/blob/main/sript.sql)


   **4. Database generation in Oracle APEX based on SQL script**

  ![image](https://github.com/IoanaFlore/Oracle-APEX---Booking-plane-tickets/assets/111995212/7a382f9f-79df-4627-9fbd-91a227c4c871)
  
## *Application development*
The application was developed using Oracle Application Express. To access the app's functionality, users are required to log in via a login page. This login page is your first interaction with the app and includes the name of the app along with a suggestive logo.

![image](https://github.com/IoanaFlore/Oracle-APEX---Booking-plane-tickets/assets/111995212/8c9e38ac-671a-4b88-8dbd-3a9b6a468925)


   1. Home page

    
The first step in the development of the application involved the development of the main pages, including the secondary ones in the menu. In addition, each page is endowed with a distinctive symbol, reflecting the associated content. The home page is the main page itself, where a suggestive image illustrating the chosen theme is integrated

  ![image](https://github.com/IoanaFlore/Oracle-APEX---Booking-plane-tickets/assets/111995212/eb24c6ef-c48d-4f0f-996e-a522d0283b75)


   2. Forms page

The main Forms page contains 5 other sub-forms as follows:

 * City form: contains a form with the necessary fields to enter the city from where the traveler wants to fly. A trigger for automatic generation was created for ID_City.
   
   ![image](https://github.com/IoanaFlore/Oracle-APEX---Booking-plane-tickets/assets/111995212/b7ce5f3a-9660-46ee-ab33-eedd08af51e7)

 * Airport form: allows the insertion of data in the AIRPORT table, but also in the CITY table. A trigger for automatic generation was created for ID_Aeroport.

   ![image](https://github.com/IoanaFlore/Oracle-APEX---Booking-plane-tickets/assets/111995212/ae857314-faf7-4efb-8ca3-a65f318312ca)

 * Company form: allows the insertion of data in the COMPANY table. A trigger for automatic generation was created for ID_Company.

   ![image](https://github.com/IoanaFlore/Oracle-APEX---Booking-plane-tickets/assets/111995212/8e461dcb-f229-472a-9e94-a02bb039c854)

 * Flights form: continue the necessary information to enter data about each flight. Thus, it allows the insertion of data in the FLIGHT table, in the AIRPORT table, and COMPANY. A trigger for automatic generation was created for ID_Flight.

   ![image](https://github.com/IoanaFlore/Oracle-APEX---Booking-plane-tickets/assets/111995212/3040bdb9-3a49-49b8-8a3e-c14239370f00)


  3. Reports page

The Reports page is the next main page, which contains 3 other sub-reports:

  * Client report – it is a simple report to check the client data if they have been entered correctly by filling out the specific form.

    ![image](https://github.com/IoanaFlore/Oracle-APEX---Booking-plane-tickets/assets/111995212/00c3b626-4af2-436f-bf3e-ac3a00e0e22e)

  * Flight report – presents data on various flights operated by certain companies. The data is related to departure dates, departure airport, flight price, company and company description. The report was made with the help of the JOIN function between the Airport, Flight, Company tables.

    ![image](https://github.com/IoanaFlore/Oracle-APEX---Booking-plane-tickets/assets/111995212/45ed23ee-3c3f-46b6-8bba-dea8885ca354)

  * Airport report - presents data about airports, the city, the country where the airport is located and the date of departure. The report was made with the help of the JOIN function between the City, Airport, Flight tables.

    ![image](https://github.com/IoanaFlore/Oracle-APEX---Booking-plane-tickets/assets/111995212/0026185d-d54c-4287-a770-1c25c0deb63f)

    
  4. Calendar page

     The Flight Calendar page was created with the aim of being able to find already scheduled flights much easier and faster

     ![image](https://github.com/IoanaFlore/Oracle-APEX---Booking-plane-tickets/assets/111995212/3d8085b5-5bc3-460c-a0ed-0701e0487db1)


 5. Flight price chart page
    
    The following chart shows the prices for each airline, oriented horizontally. The names of the companies are listed on the vertical axis (Oy), while the prices expressed in lei are represented on the horizontal axis (Ox).

    ![image](https://github.com/IoanaFlore/Oracle-APEX---Booking-plane-tickets/assets/111995212/d5e6010a-a6a2-49eb-a963-32c471065c61)


#### Access to the application is made through the following link: [access to the application](https://apex.oracle.com/pls/apex/r/ioanaflore99/aeroport/login?session=100580728154733)

Login credentials:

Username: ioanamarincas993@gmail.com
Password: marincasioaflore9


