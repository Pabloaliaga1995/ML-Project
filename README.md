# Project-m3
ESP

OBJETIVO

Conseguir un modelo de predicción de la base de datos con la que trabajamos en el anterior proyecto (diamonds)

ENV
Hemos creado un nuevo entorno (project3), instalado e importado (import + "name of the library"):

- Python 3.7 (conda install python == 3.7)
- Pandas (conda install pandas)
- Sqlalchemy (conda install sqlalchemy)
- Sqlite 3 (conda install sqlite)
- matplotlib
- sklearn

CODE 
En primer lugar, hemos importado la base de datos:
diamonds_train.db
Después de importar la base de datos, mediante inner joins hemos conseguido una nueva tabla, la cual hemos exportado a un dataframe mediante Pandas.
Posteriormente hemos guardado el dataframe como CSV para poder comenzar a trabajar con el.

Hemos definido una función para eliminar los outliers (remove_outlier) y conseguir una mejor predicción.
A continuación importamos el dataset de test y definimos target y features para ambos datasets.
Categorizamos las features para trabajar con ellas posteriormente.

Una vez hecho esto, sacamos mediante get_dummies las features categóricas y añadimos las features numéricas a dos nuevos dataframes (train_df y test_df).

Sobre nuestros dos nuevos dataframes, aplicamos el scaler y entrenamos el modelo mediante train_test_split.

Tras utilizar numerosos modelos, como linear_model, ElasticNet, GradientBoostingRegressor, hemos optado por utilizar RandomForestRegressor, ya que, despues de hacer fit sobre nuestro modelo entrenado, sacamos la predicción mediante este modelo (regressor)

Con esto, nos daba una rmse de 566, que hemos subido a kaggle a través de la submissión guardada.

ENG

OBJECTIVE

To obtain a predictive model of the database we had worked with in the previous project (diamonds).

ENV
We have created a new environment (project3), installed and imported (import + "name of the library"):

- Python 3.7 (conda install python == 3.7).
- Pandas (conda install pandas)
- Sqlalchemy (conda install sqlalchemy)
- Sqlite 3 (conda install sqlite)
- matplotlib
- sklearn

CODE 
First, we have imported the database:
diamonds_train.db
After importing the database, using inner joins, we got a new table, which we exported to a dataframe using Pandas.
We save the dataframe as CSV to be able to start working with it.

We have defined a function to remove the outliers (remove_outlier) and get a better prediction.
Then we import the test dataset and define the target and features for both datasets.
We categorize the features to work with them later.

Once we have this done, we get the categorical features using get_dummies and add the numerical features to two new dataframes (train_df and test_df).

On our two new dataframes, we apply the scaler and train the model using train_test_split.

After using some models, such as linear_model, ElasticNet, GradientBoostingRegressor, we chose to use RandomForestRegressor, and, after fitting our trained model, we got the prediction using this model (regressor).

With this model, we obtained an rmse of 566, which we uploaded to kaggle through the saved submission.