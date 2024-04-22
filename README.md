To get started with BizCardX Data Extraction, follow the steps below:

Install the required libraries using the pip install command. Streamlit, mysql.connector, pandas, easyocr.

pip install [Name of the library]
By using streamlit, I have created the app with three menu options namely HOME, UPLOAD & EXTRACT, MODIFY where user has the option to upload the respective Business Card whose information has to be extracted, stored, modified or deleted if needed.

Home upload modify

Once user uploads a business card, the text present in the card is extracted by easyocr library.

The extracted text is sent to get_data() function(user defined- I have coded this function) for respective text classification as company name, card holder name, designation, mobile number, email address, website URL, area, city, state, and pin code using loops and some regular expression.

The classified data is displayed on screen which can be further edited by user based on requirement.

On Clicking Upload to Database Button the data gets stored in the MySQL Database. (Note: Provide respective host, user, password, database name in create_database, sql_table_creation and connect_database for establishing connection.)

Further with the help of MODIFY menu the uploaded data’s in SQL Database can be accessed for Read, Update and Delete Operations.
