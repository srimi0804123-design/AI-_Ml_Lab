# AI-_Ml_Lab
A repository that consists of the tasks done in lab
.
{
 "cells": [
  {
   "cell_type": "code",
   "execution_count": 2,
   "id": "453fd2f4-352b-4321-9b1b-e7c97b5dff96",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>patient_id</th>\n",
       "      <th>name</th>\n",
       "      <th>age</th>\n",
       "      <th>gender</th>\n",
       "      <th>city</th>\n",
       "      <th>admission_date</th>\n",
       "      <th>height_cm</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>P001</td>\n",
       "      <td>NaN</td>\n",
       "      <td>25.0</td>\n",
       "      <td>F</td>\n",
       "      <td>mumbai</td>\n",
       "      <td>15-01-2024</td>\n",
       "      <td>180</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>P002</td>\n",
       "      <td>Rahul Sharma</td>\n",
       "      <td>60.0</td>\n",
       "      <td>F</td>\n",
       "      <td>Delhi</td>\n",
       "      <td>16-01-2024</td>\n",
       "      <td>170</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>P003</td>\n",
       "      <td>Neha Singh</td>\n",
       "      <td>45.0</td>\n",
       "      <td>M</td>\n",
       "      <td>Mumbai</td>\n",
       "      <td>16-01-2024</td>\n",
       "      <td>150</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>P004</td>\n",
       "      <td>Neha Singh</td>\n",
       "      <td>60.0</td>\n",
       "      <td>Male</td>\n",
       "      <td>kolkata</td>\n",
       "      <td>15-01-2024</td>\n",
       "      <td>170</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4</th>\n",
       "      <td>P005</td>\n",
       "      <td>Neha Singh</td>\n",
       "      <td>25.0</td>\n",
       "      <td>Male</td>\n",
       "      <td>kolkata</td>\n",
       "      <td>15-01-2024</td>\n",
       "      <td>180</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>...</th>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>125</th>\n",
       "      <td>P006</td>\n",
       "      <td>Anita Verma</td>\n",
       "      <td>25.0</td>\n",
       "      <td>M</td>\n",
       "      <td>Mumbai</td>\n",
       "      <td>15-01-2024</td>\n",
       "      <td>150</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>126</th>\n",
       "      <td>P007</td>\n",
       "      <td>Neha Singh</td>\n",
       "      <td>25.0</td>\n",
       "      <td>F</td>\n",
       "      <td>kolkata</td>\n",
       "      <td>15-01-2024</td>\n",
       "      <td>150</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>127</th>\n",
       "      <td>P008</td>\n",
       "      <td>John Paul</td>\n",
       "      <td>60.0</td>\n",
       "      <td>F</td>\n",
       "      <td>Chennai</td>\n",
       "      <td>15-01-2024</td>\n",
       "      <td>160</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>128</th>\n",
       "      <td>P009</td>\n",
       "      <td>NaN</td>\n",
       "      <td>45.0</td>\n",
       "      <td>M</td>\n",
       "      <td>Mumbai</td>\n",
       "      <td>15-01-2024</td>\n",
       "      <td>150</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>129</th>\n",
       "      <td>P010</td>\n",
       "      <td>Rahul Sharma</td>\n",
       "      <td>60.0</td>\n",
       "      <td>Female</td>\n",
       "      <td>Chennai</td>\n",
       "      <td>16-01-2024</td>\n",
       "      <td>150</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "<p>130 rows × 7 columns</p>\n",
       "</div>"
      ],
      "text/plain": [
       "    patient_id          name   age  gender     city admission_date height_cm\n",
       "0         P001           NaN  25.0       F   mumbai     15-01-2024       180\n",
       "1         P002  Rahul Sharma  60.0       F    Delhi     16-01-2024       170\n",
       "2         P003    Neha Singh  45.0       M   Mumbai     16-01-2024       150\n",
       "3         P004    Neha Singh  60.0    Male  kolkata     15-01-2024       170\n",
       "4         P005    Neha Singh  25.0    Male  kolkata     15-01-2024       180\n",
       "..         ...           ...   ...     ...      ...            ...       ...\n",
       "125       P006   Anita Verma  25.0       M   Mumbai     15-01-2024       150\n",
       "126       P007    Neha Singh  25.0       F  kolkata     15-01-2024       150\n",
       "127       P008     John Paul  60.0       F  Chennai     15-01-2024       160\n",
       "128       P009           NaN  45.0       M   Mumbai     15-01-2024       150\n",
       "129       P010  Rahul Sharma  60.0  Female  Chennai     16-01-2024       150\n",
       "\n",
       "[130 rows x 7 columns]"
      ]
     },
     "execution_count": 2,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "import pandas as pd\n",
    "df=pd.read_csv(r\"C:\\Users\\Srimi\\OneDrive\\Desktop\\file1.csv\")\n",
    "df"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 3,
   "id": "aad80249-8c2c-4d49-8152-2d5d4dade6d2",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>patient_id</th>\n",
       "      <th>name</th>\n",
       "      <th>age</th>\n",
       "      <th>gender</th>\n",
       "      <th>city</th>\n",
       "      <th>admission_date</th>\n",
       "      <th>height_cm</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>P001</td>\n",
       "      <td>NaN</td>\n",
       "      <td>25.0</td>\n",
       "      <td>F</td>\n",
       "      <td>mumbai</td>\n",
       "      <td>15-01-2024</td>\n",
       "      <td>180</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>P002</td>\n",
       "      <td>Rahul Sharma</td>\n",
       "      <td>60.0</td>\n",
       "      <td>F</td>\n",
       "      <td>Delhi</td>\n",
       "      <td>16-01-2024</td>\n",
       "      <td>170</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>P003</td>\n",
       "      <td>Neha Singh</td>\n",
       "      <td>45.0</td>\n",
       "      <td>M</td>\n",
       "      <td>Mumbai</td>\n",
       "      <td>16-01-2024</td>\n",
       "      <td>150</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>P004</td>\n",
       "      <td>Neha Singh</td>\n",
       "      <td>60.0</td>\n",
       "      <td>Male</td>\n",
       "      <td>kolkata</td>\n",
       "      <td>15-01-2024</td>\n",
       "      <td>170</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4</th>\n",
       "      <td>P005</td>\n",
       "      <td>Neha Singh</td>\n",
       "      <td>25.0</td>\n",
       "      <td>Male</td>\n",
       "      <td>kolkata</td>\n",
       "      <td>15-01-2024</td>\n",
       "      <td>180</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "  patient_id          name   age gender     city admission_date height_cm\n",
       "0       P001           NaN  25.0      F   mumbai     15-01-2024       180\n",
       "1       P002  Rahul Sharma  60.0      F    Delhi     16-01-2024       170\n",
       "2       P003    Neha Singh  45.0      M   Mumbai     16-01-2024       150\n",
       "3       P004    Neha Singh  60.0   Male  kolkata     15-01-2024       170\n",
       "4       P005    Neha Singh  25.0   Male  kolkata     15-01-2024       180"
      ]
     },
     "execution_count": 3,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df.head()\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 4,
   "id": "13a23dee-a634-481b-b71b-b395c4eda0b4",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>patient_id</th>\n",
       "      <th>name</th>\n",
       "      <th>age</th>\n",
       "      <th>gender</th>\n",
       "      <th>city</th>\n",
       "      <th>admission_date</th>\n",
       "      <th>height_cm</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>125</th>\n",
       "      <td>P006</td>\n",
       "      <td>Anita Verma</td>\n",
       "      <td>25.0</td>\n",
       "      <td>M</td>\n",
       "      <td>Mumbai</td>\n",
       "      <td>15-01-2024</td>\n",
       "      <td>150</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>126</th>\n",
       "      <td>P007</td>\n",
       "      <td>Neha Singh</td>\n",
       "      <td>25.0</td>\n",
       "      <td>F</td>\n",
       "      <td>kolkata</td>\n",
       "      <td>15-01-2024</td>\n",
       "      <td>150</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>127</th>\n",
       "      <td>P008</td>\n",
       "      <td>John Paul</td>\n",
       "      <td>60.0</td>\n",
       "      <td>F</td>\n",
       "      <td>Chennai</td>\n",
       "      <td>15-01-2024</td>\n",
       "      <td>160</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>128</th>\n",
       "      <td>P009</td>\n",
       "      <td>NaN</td>\n",
       "      <td>45.0</td>\n",
       "      <td>M</td>\n",
       "      <td>Mumbai</td>\n",
       "      <td>15-01-2024</td>\n",
       "      <td>150</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>129</th>\n",
       "      <td>P010</td>\n",
       "      <td>Rahul Sharma</td>\n",
       "      <td>60.0</td>\n",
       "      <td>Female</td>\n",
       "      <td>Chennai</td>\n",
       "      <td>16-01-2024</td>\n",
       "      <td>150</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "    patient_id          name   age  gender     city admission_date height_cm\n",
       "125       P006   Anita Verma  25.0       M   Mumbai     15-01-2024       150\n",
       "126       P007    Neha Singh  25.0       F  kolkata     15-01-2024       150\n",
       "127       P008     John Paul  60.0       F  Chennai     15-01-2024       160\n",
       "128       P009           NaN  45.0       M   Mumbai     15-01-2024       150\n",
       "129       P010  Rahul Sharma  60.0  Female  Chennai     16-01-2024       150"
      ]
     },
     "execution_count": 4,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df.tail()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 5,
   "id": "f1f651e8-f847-423c-a671-915bac093adb",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "2"
      ]
     },
     "execution_count": 5,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df.ndim"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 6,
   "id": "e6c16dd2-2053-415f-8283-3adbf538d227",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "910"
      ]
     },
     "execution_count": 6,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df.size"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 7,
   "id": "f5b61fd8-e3b9-4f9f-b990-39d47679315e",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "(130, 7)"
      ]
     },
     "execution_count": 7,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df.shape"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 8,
   "id": "b98c20a5-5ae9-4c39-8cd7-f38987490b3d",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>age</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>count</th>\n",
       "      <td>106.000000</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>mean</th>\n",
       "      <td>35.849057</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>std</th>\n",
       "      <td>21.015546</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>min</th>\n",
       "      <td>-5.000000</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>25%</th>\n",
       "      <td>25.000000</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>50%</th>\n",
       "      <td>30.000000</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>75%</th>\n",
       "      <td>60.000000</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>max</th>\n",
       "      <td>60.000000</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "              age\n",
       "count  106.000000\n",
       "mean    35.849057\n",
       "std     21.015546\n",
       "min     -5.000000\n",
       "25%     25.000000\n",
       "50%     30.000000\n",
       "75%     60.000000\n",
       "max     60.000000"
      ]
     },
     "execution_count": 8,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df.describe()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 9,
   "id": "a6921cdd-fbe7-4f16-b9af-f8245d44e13d",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>patient_id</th>\n",
       "      <th>name</th>\n",
       "      <th>age</th>\n",
       "      <th>gender</th>\n",
       "      <th>city</th>\n",
       "      <th>admission_date</th>\n",
       "      <th>height_cm</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>False</td>\n",
       "      <td>True</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4</th>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>...</th>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>125</th>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>126</th>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>127</th>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>128</th>\n",
       "      <td>False</td>\n",
       "      <td>True</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>129</th>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "<p>130 rows × 7 columns</p>\n",
       "</div>"
      ],
      "text/plain": [
       "     patient_id   name    age  gender   city  admission_date  height_cm\n",
       "0         False   True  False   False  False           False      False\n",
       "1         False  False  False   False  False           False      False\n",
       "2         False  False  False   False  False           False      False\n",
       "3         False  False  False   False  False           False      False\n",
       "4         False  False  False   False  False           False      False\n",
       "..          ...    ...    ...     ...    ...             ...        ...\n",
       "125       False  False  False   False  False           False      False\n",
       "126       False  False  False   False  False           False      False\n",
       "127       False  False  False   False  False           False      False\n",
       "128       False   True  False   False  False           False      False\n",
       "129       False  False  False   False  False           False      False\n",
       "\n",
       "[130 rows x 7 columns]"
      ]
     },
     "execution_count": 9,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df.isnull()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 11,
   "id": "0f24c4f1-aa0f-4050-adaf-9fe764b67f85",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "<bound method DataFrame.sum of      patient_id   name    age  gender   city  admission_date  height_cm\n",
       "0         False   True  False   False  False           False      False\n",
       "1         False  False  False   False  False           False      False\n",
       "2         False  False  False   False  False           False      False\n",
       "3         False  False  False   False  False           False      False\n",
       "4         False  False  False   False  False           False      False\n",
       "..          ...    ...    ...     ...    ...             ...        ...\n",
       "125       False  False  False   False  False           False      False\n",
       "126       False  False  False   False  False           False      False\n",
       "127       False  False  False   False  False           False      False\n",
       "128       False   True  False   False  False           False      False\n",
       "129       False  False  False   False  False           False      False\n",
       "\n",
       "[130 rows x 7 columns]>"
      ]
     },
     "execution_count": 11,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df.isnull().sum"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 12,
   "id": "d48bc1c5-23d3-45ac-8c34-e504868d2ab3",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "0                 x\n",
       "1      Rahul Sharma\n",
       "2        Neha Singh\n",
       "3        Neha Singh\n",
       "4        Neha Singh\n",
       "           ...     \n",
       "125     Anita Verma\n",
       "126      Neha Singh\n",
       "127       John Paul\n",
       "128               x\n",
       "129    Rahul Sharma\n",
       "Name: name, Length: 130, dtype: str"
      ]
     },
     "execution_count": 12,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df[\"name\"].fillna(\"x\")"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 13,
   "id": "aaed06ee-e5df-4ab8-97f1-419e9e994721",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>patient_id</th>\n",
       "      <th>name</th>\n",
       "      <th>age</th>\n",
       "      <th>gender</th>\n",
       "      <th>city</th>\n",
       "      <th>admission_date</th>\n",
       "      <th>height_cm</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>False</td>\n",
       "      <td>True</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4</th>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>...</th>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>125</th>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>126</th>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>127</th>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>128</th>\n",
       "      <td>False</td>\n",
       "      <td>True</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>129</th>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "      <td>False</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "<p>130 rows × 7 columns</p>\n",
       "</div>"
      ],
      "text/plain": [
       "     patient_id   name    age  gender   city  admission_date  height_cm\n",
       "0         False   True  False   False  False           False      False\n",
       "1         False  False  False   False  False           False      False\n",
       "2         False  False  False   False  False           False      False\n",
       "3         False  False  False   False  False           False      False\n",
       "4         False  False  False   False  False           False      False\n",
       "..          ...    ...    ...     ...    ...             ...        ...\n",
       "125       False  False  False   False  False           False      False\n",
       "126       False  False  False   False  False           False      False\n",
       "127       False  False  False   False  False           False      False\n",
       "128       False   True  False   False  False           False      False\n",
       "129       False  False  False   False  False           False      False\n",
       "\n",
       "[130 rows x 7 columns]"
      ]
     },
     "execution_count": 13,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df.isna()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 16,
   "id": "2b93c1aa-4c85-4dea-997a-36764e897dfe",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>record_id</th>\n",
       "      <th>patient_id</th>\n",
       "      <th>diagnosis</th>\n",
       "      <th>bp</th>\n",
       "      <th>sugar_level</th>\n",
       "      <th>visit_cost</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>R101</td>\n",
       "      <td>P013</td>\n",
       "      <td>Hypertension</td>\n",
       "      <td>120/80</td>\n",
       "      <td>140.0</td>\n",
       "      <td>2000</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>R102</td>\n",
       "      <td>P105</td>\n",
       "      <td>Diabetes</td>\n",
       "      <td>120/80</td>\n",
       "      <td>NaN</td>\n",
       "      <td>2500</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>R103</td>\n",
       "      <td>P098</td>\n",
       "      <td>Hypertension</td>\n",
       "      <td>high</td>\n",
       "      <td>140.0</td>\n",
       "      <td>3000</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>R104</td>\n",
       "      <td>P038</td>\n",
       "      <td>Asthma</td>\n",
       "      <td>140/90</td>\n",
       "      <td>NaN</td>\n",
       "      <td>3000</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4</th>\n",
       "      <td>R105</td>\n",
       "      <td>P040</td>\n",
       "      <td>Asthma</td>\n",
       "      <td>130/85</td>\n",
       "      <td>NaN</td>\n",
       "      <td>1500</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>...</th>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>115</th>\n",
       "      <td>R216</td>\n",
       "      <td>P081</td>\n",
       "      <td>Asthma</td>\n",
       "      <td>high</td>\n",
       "      <td>110.0</td>\n",
       "      <td>2500</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>116</th>\n",
       "      <td>R217</td>\n",
       "      <td>P033</td>\n",
       "      <td>Diabetes</td>\n",
       "      <td>high</td>\n",
       "      <td>NaN</td>\n",
       "      <td>1500</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>117</th>\n",
       "      <td>R218</td>\n",
       "      <td>P063</td>\n",
       "      <td>Hypertension</td>\n",
       "      <td>140/90</td>\n",
       "      <td>NaN</td>\n",
       "      <td>2000</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>118</th>\n",
       "      <td>R219</td>\n",
       "      <td>P011</td>\n",
       "      <td>Hypertension</td>\n",
       "      <td>130/85</td>\n",
       "      <td>180.0</td>\n",
       "      <td>2500</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>119</th>\n",
       "      <td>R220</td>\n",
       "      <td>P013</td>\n",
       "      <td>Hypertension</td>\n",
       "      <td>high</td>\n",
       "      <td>180.0</td>\n",
       "      <td>1500</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "<p>120 rows × 6 columns</p>\n",
       "</div>"
      ],
      "text/plain": [
       "    record_id patient_id     diagnosis      bp  sugar_level  visit_cost\n",
       "0        R101       P013  Hypertension  120/80        140.0        2000\n",
       "1        R102       P105      Diabetes  120/80          NaN        2500\n",
       "2        R103       P098  Hypertension    high        140.0        3000\n",
       "3        R104       P038        Asthma  140/90          NaN        3000\n",
       "4        R105       P040        Asthma  130/85          NaN        1500\n",
       "..        ...        ...           ...     ...          ...         ...\n",
       "115      R216       P081        Asthma    high        110.0        2500\n",
       "116      R217       P033      Diabetes    high          NaN        1500\n",
       "117      R218       P063  Hypertension  140/90          NaN        2000\n",
       "118      R219       P011  Hypertension  130/85        180.0        2500\n",
       "119      R220       P013  Hypertension    high        180.0        1500\n",
       "\n",
       "[120 rows x 6 columns]"
      ]
     },
     "execution_count": 16,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df=pd.read_csv(r\"C:\\Users\\Srimi\\OneDrive\\Desktop\\file2.csv\")\n",
    "df"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 19,
   "id": "9d7f7fff-6823-4bcd-bc84-fee48b990fa1",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "Index(['record_id', 'patient_id', 'diagnosis', 'bp', 'sugar_level',\n",
       "       'visit_cost'],\n",
       "      dtype='str')"
      ]
     },
     "execution_count": 19,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df.columns"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 21,
   "id": "06764edc-feee-4c65-ab0e-163a0de56718",
   "metadata": {
    "scrolled": true
   },
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>record_id</th>\n",
       "      <th>patient_id</th>\n",
       "      <th>diagnosis</th>\n",
       "      <th>bp</th>\n",
       "      <th>sugar_level</th>\n",
       "      <th>visit_cost</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>R101</td>\n",
       "      <td>P013</td>\n",
       "      <td>Hypertension</td>\n",
       "      <td>120/80</td>\n",
       "      <td>140.0</td>\n",
       "      <td>2000</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>R102</td>\n",
       "      <td>P105</td>\n",
       "      <td>Diabetes</td>\n",
       "      <td>120/80</td>\n",
       "      <td>0.0</td>\n",
       "      <td>2500</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>R103</td>\n",
       "      <td>P098</td>\n",
       "      <td>Hypertension</td>\n",
       "      <td>high</td>\n",
       "      <td>140.0</td>\n",
       "      <td>3000</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>R104</td>\n",
       "      <td>P038</td>\n",
       "      <td>Asthma</td>\n",
       "      <td>140/90</td>\n",
       "      <td>0.0</td>\n",
       "      <td>3000</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4</th>\n",
       "      <td>R105</td>\n",
       "      <td>P040</td>\n",
       "      <td>Asthma</td>\n",
       "      <td>130/85</td>\n",
       "      <td>0.0</td>\n",
       "      <td>1500</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>...</th>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>115</th>\n",
       "      <td>R216</td>\n",
       "      <td>P081</td>\n",
       "      <td>Asthma</td>\n",
       "      <td>high</td>\n",
       "      <td>110.0</td>\n",
       "      <td>2500</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>116</th>\n",
       "      <td>R217</td>\n",
       "      <td>P033</td>\n",
       "      <td>Diabetes</td>\n",
       "      <td>high</td>\n",
       "      <td>0.0</td>\n",
       "      <td>1500</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>117</th>\n",
       "      <td>R218</td>\n",
       "      <td>P063</td>\n",
       "      <td>Hypertension</td>\n",
       "      <td>140/90</td>\n",
       "      <td>0.0</td>\n",
       "      <td>2000</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>118</th>\n",
       "      <td>R219</td>\n",
       "      <td>P011</td>\n",
       "      <td>Hypertension</td>\n",
       "      <td>130/85</td>\n",
       "      <td>180.0</td>\n",
       "      <td>2500</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>119</th>\n",
       "      <td>R220</td>\n",
       "      <td>P013</td>\n",
       "      <td>Hypertension</td>\n",
       "      <td>high</td>\n",
       "      <td>180.0</td>\n",
       "      <td>1500</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "<p>120 rows × 6 columns</p>\n",
       "</div>"
      ],
      "text/plain": [
       "    record_id patient_id     diagnosis      bp  sugar_level  visit_cost\n",
       "0        R101       P013  Hypertension  120/80        140.0        2000\n",
       "1        R102       P105      Diabetes  120/80          0.0        2500\n",
       "2        R103       P098  Hypertension    high        140.0        3000\n",
       "3        R104       P038        Asthma  140/90          0.0        3000\n",
       "4        R105       P040        Asthma  130/85          0.0        1500\n",
       "..        ...        ...           ...     ...          ...         ...\n",
       "115      R216       P081        Asthma    high        110.0        2500\n",
       "116      R217       P033      Diabetes    high          0.0        1500\n",
       "117      R218       P063  Hypertension  140/90          0.0        2000\n",
       "118      R219       P011  Hypertension  130/85        180.0        2500\n",
       "119      R220       P013  Hypertension    high        180.0        1500\n",
       "\n",
       "[120 rows x 6 columns]"
      ]
     },
     "execution_count": 21,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df.fillna({\"sugar_level\": 0}, inplace=True)\n",
    "df"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 25,
   "id": "1becd018-e22d-49d5-9b53-4403f64ef22f",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "<bound method NDFrame.describe of     record_id patient_id     diagnosis      bp  sugar_level  visit_cost\n",
       "0        R101       P013  Hypertension  120/80        140.0        2000\n",
       "1        R102       P105      Diabetes  120/80          0.0        2500\n",
       "2        R103       P098  Hypertension    high        140.0        3000\n",
       "3        R104       P038        Asthma  140/90          0.0        3000\n",
       "4        R105       P040        Asthma  130/85          0.0        1500\n",
       "..        ...        ...           ...     ...          ...         ...\n",
       "115      R216       P081        Asthma    high        110.0        2500\n",
       "116      R217       P033      Diabetes    high          0.0        1500\n",
       "117      R218       P063  Hypertension  140/90          0.0        2000\n",
       "118      R219       P011  Hypertension  130/85        180.0        2500\n",
       "119      R220       P013  Hypertension    high        180.0        1500\n",
       "\n",
       "[120 rows x 6 columns]>"
      ]
     },
     "execution_count": 25,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df.describe"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 26,
   "id": "f7f3558b-5c85-45cd-a5f0-4919e92f3d36",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "diagnosis\n",
       "Asthma          2242.857143\n",
       "Diabetes        2220.930233\n",
       "Hypertension    2392.857143\n",
       "Name: visit_cost, dtype: float64"
      ]
     },
     "execution_count": 26,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df.groupby('diagnosis')['visit_cost'].mean()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 27,
   "id": "23d17f21-4af7-4155-bc9e-41097cb3c818",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "diagnosis\n",
       "Diabetes        43\n",
       "Hypertension    42\n",
       "Asthma          35\n",
       "Name: count, dtype: int64"
      ]
     },
     "execution_count": 27,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df[\"diagnosis\"].value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 28,
   "id": "2949802d-b00c-4921-990f-8d6a9cd5f1fe",
   "metadata": {},
   "outputs": [],
   "source": [
    "df[\"bp\"]= df[\"bp\"].replace(\"high\",'140/90')\n",
    "df[\"bp\"]= df[\"bp\"].replace(\"low\",'90/60')"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 29,
   "id": "ddcddf2b-ebdb-4b58-8211-660c55f2a392",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "0      120/80\n",
       "1      120/80\n",
       "2      140/90\n",
       "3      140/90\n",
       "4      130/85\n",
       "        ...  \n",
       "115    140/90\n",
       "116    140/90\n",
       "117    140/90\n",
       "118    130/85\n",
       "119    140/90\n",
       "Name: bp, Length: 120, dtype: str"
      ]
     },
     "execution_count": 29,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df['bp']"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 30,
   "id": "a256f40a-1c7c-423c-82f2-204f93d226b6",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "diagnosis     bp    \n",
       "Asthma        140/90    20\n",
       "              130/85     9\n",
       "              120/80     6\n",
       "Diabetes      140/90    28\n",
       "              130/85     8\n",
       "              120/80     7\n",
       "Hypertension  140/90    19\n",
       "              130/85    15\n",
       "              120/80     8\n",
       "Name: count, dtype: int64"
      ]
     },
     "execution_count": 30,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df.groupby('diagnosis')[\"bp\"].value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 31,
   "id": "877832a9-b3e3-418d-af0d-f37b2df22f2a",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "np.float64(180.0)"
      ]
     },
     "execution_count": 31,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df[\"sugar_level\"].max()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 32,
   "id": "770379c8-89bb-4453-b92d-7c296e4a5f10",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "np.float64(0.0)"
      ]
     },
     "execution_count": 32,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df[\"sugar_level\"].min()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 33,
   "id": "d2112830-9041-47cd-99cd-d73952b635ed",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "np.int64(1500)"
      ]
     },
     "execution_count": 33,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df[\"visit_cost\"].min()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 34,
   "id": "eb7caaf7-53c1-429d-ae8a-b25a38e87f93",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "np.int64(3000)"
      ]
     },
     "execution_count": 34,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df[\"visit_cost\"].max()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 35,
   "id": "5ec9587c-20bb-4861-bb79-a262d9fb2c00",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "diagnosis\n",
       "Asthma          2242.857143\n",
       "Diabetes        2220.930233\n",
       "Hypertension    2392.857143\n",
       "Name: visit_cost, dtype: float64"
      ]
     },
     "execution_count": 35,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df.groupby('diagnosis')['visit_cost'].mean()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 36,
   "id": "11590873-8726-499d-9617-6e0f768833b3",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "diagnosis\n",
       "Asthma           83.142857\n",
       "Diabetes        109.767442\n",
       "Hypertension    103.809524\n",
       "Name: sugar_level, dtype: float64"
      ]
     },
     "execution_count": 36,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df.groupby(\"diagnosis\")[\"sugar_level\"].mean()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 37,
   "id": "3fa1d801-20ff-4bc5-a250-8420ed1f4001",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "diagnosis\n",
       "Diabetes        43\n",
       "Hypertension    42\n",
       "Asthma          35\n",
       "Name: count, dtype: int64"
      ]
     },
     "execution_count": 37,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df[\"diagnosis\"].value_counts()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 38,
   "id": "6e393d06-8e3b-41e5-9b8e-b7e6ed6194bd",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "record_id      0\n",
       "patient_id     0\n",
       "diagnosis      0\n",
       "bp             0\n",
       "sugar_level    0\n",
       "visit_cost     0\n",
       "dtype: int64"
      ]
     },
     "execution_count": 38,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df.isnull().sum()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 39,
   "id": "e3aade76-73ff-4d0c-a203-e07998cf61a4",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "<bound method NDFrame.describe of     record_id patient_id     diagnosis      bp  sugar_level  visit_cost\n",
       "0        R101       P013  Hypertension  120/80        140.0        2000\n",
       "1        R102       P105      Diabetes  120/80          0.0        2500\n",
       "2        R103       P098  Hypertension  140/90        140.0        3000\n",
       "3        R104       P038        Asthma  140/90          0.0        3000\n",
       "4        R105       P040        Asthma  130/85          0.0        1500\n",
       "..        ...        ...           ...     ...          ...         ...\n",
       "115      R216       P081        Asthma  140/90        110.0        2500\n",
       "116      R217       P033      Diabetes  140/90          0.0        1500\n",
       "117      R218       P063  Hypertension  140/90          0.0        2000\n",
       "118      R219       P011  Hypertension  130/85        180.0        2500\n",
       "119      R220       P013  Hypertension  140/90        180.0        1500\n",
       "\n",
       "[120 rows x 6 columns]>"
      ]
     },
     "execution_count": 39,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df.describe"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 40,
   "id": "5e73dd41-d837-41f5-828a-94a373ea25ce",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "<class 'pandas.DataFrame'>\n",
      "RangeIndex: 120 entries, 0 to 119\n",
      "Data columns (total 6 columns):\n",
      " #   Column       Non-Null Count  Dtype  \n",
      "---  ------       --------------  -----  \n",
      " 0   record_id    120 non-null    str    \n",
      " 1   patient_id   120 non-null    str    \n",
      " 2   diagnosis    120 non-null    str    \n",
      " 3   bp           120 non-null    str    \n",
      " 4   sugar_level  120 non-null    float64\n",
      " 5   visit_cost   120 non-null    int64  \n",
      "dtypes: float64(1), int64(1), str(4)\n",
      "memory usage: 5.8 KB\n"
     ]
    }
   ],
   "source": [
    "df.info()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 41,
   "id": "e85f8bb9-2f30-4578-b309-5769fc0336ff",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>student_id</th>\n",
       "      <th>name</th>\n",
       "      <th>age</th>\n",
       "      <th>subject</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>101</td>\n",
       "      <td>Alice</td>\n",
       "      <td>20</td>\n",
       "      <td>Math</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>102</td>\n",
       "      <td>Bob</td>\n",
       "      <td>21</td>\n",
       "      <td>Math</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>103</td>\n",
       "      <td>Charlie</td>\n",
       "      <td>19</td>\n",
       "      <td>Math</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>104</td>\n",
       "      <td>David</td>\n",
       "      <td>22</td>\n",
       "      <td>Math</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "   student_id     name  age subject\n",
       "0         101    Alice   20    Math\n",
       "1         102      Bob   21    Math\n",
       "2         103  Charlie   19    Math\n",
       "3         104    David   22    Math"
      ]
     },
     "execution_count": 41,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "import pandas as pd\n",
    "import numpy as np\n",
    "import matplotlib.pyplot as plt\n",
    "import seaborn as sns\n",
    "data = {\n",
    "    \"student_id\": [101, 102, 103, 104],\n",
    "    \"name\": [\"Alice\", \"Bob\", \"Charlie\", \"David\"],\n",
    "    \"age\": [20, 21, 19, 22],\n",
    "    \"subject\": [\"Math\", \"Math\", \"Math\", \"Math\"]\n",
    "}\n",
    "\n",
    "df = pd.DataFrame(data)\n",
    "df\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 42,
   "id": "1048f5ef-3f88-4f4f-844a-20fc5aa52213",
   "metadata": {},
   "outputs": [
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter marks for Alice:  45\n",
      "Enter marks for Bob:  77\n",
      "Enter marks for Charlie:  90\n",
      "Enter marks for David:  67\n"
     ]
    },
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>student_id</th>\n",
       "      <th>name</th>\n",
       "      <th>age</th>\n",
       "      <th>subject</th>\n",
       "      <th>marks</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>101</td>\n",
       "      <td>Alice</td>\n",
       "      <td>20</td>\n",
       "      <td>Math</td>\n",
       "      <td>45</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>102</td>\n",
       "      <td>Bob</td>\n",
       "      <td>21</td>\n",
       "      <td>Math</td>\n",
       "      <td>77</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>103</td>\n",
       "      <td>Charlie</td>\n",
       "      <td>19</td>\n",
       "      <td>Math</td>\n",
       "      <td>90</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>104</td>\n",
       "      <td>David</td>\n",
       "      <td>22</td>\n",
       "      <td>Math</td>\n",
       "      <td>67</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "   student_id     name  age subject  marks\n",
       "0         101    Alice   20    Math     45\n",
       "1         102      Bob   21    Math     77\n",
       "2         103  Charlie   19    Math     90\n",
       "3         104    David   22    Math     67"
      ]
     },
     "execution_count": 42,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "marks = []\n",
    "\n",
    "for name in df[\"name\"]:\n",
    "    mark = int(input(f\"Enter marks for {name}: \"))\n",
    "    marks.append(mark)\n",
    "\n",
    "df[\"marks\"] = np.array(marks)\n",
    "df\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 43,
   "id": "be71f9bc-37a6-4133-b99a-259e50a727d2",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": "iVBORw0KGgoAAAANSUhEUgAAAjIAAAHHCAYAAACle7JuAAAAOnRFWHRTb2Z0d2FyZQBNYXRwbG90bGliIHZlcnNpb24zLjEwLjgsIGh0dHBzOi8vbWF0cGxvdGxpYi5vcmcvwVt1zgAAAAlwSFlzAAAPYQAAD2EBqD+naQAANBdJREFUeJzt3Qm8zGX///GPY9/3tXBUCiFbhZSSUpaQKD8VpVS0aBP3Q7q1KZUQcVOJ0sJtKSlyI+pOKqRSaRNKaEOR/ft/vK/7MfOfOeY4i2HmOuf1fDzGMfs1852Z7/t7XZ/r+80TBEFgAAAAHkpJdAMAAACyiyADAAC8RZABAADeIsgAAABvEWQAAIC3CDIAAMBbBBkAAOAtggwAAPAWQQYAAHiLIAPEwQ8//GB58uSxxx9/POHv55YtW+yyyy6zsmXLujaNHDnSklmvXr0sNTXVfHTw4EGrW7euPfTQQ4luinf++c9/us/nr7/+etjb7du3z6pWrWpPP/30MWsb/EKQQY7x/PPPux9Gnd57771DrtfROPSDqOvbt29vOdXtt99u8+fPt0GDBtkLL7xgF110Ubq3/euvv+y+++5zK+OiRYu68NOgQQO77bbbbNOmTeHbvfnmm27F46svvvjCtV+BM55efvll27hxo918880xP4ehU4UKFey8886zt956y461OXPmWIcOHaxixYpWoEABK1OmjJ1zzjn2xBNP2I4dOyzZ5c+f3+644w4XFnfv3p3o5iAJEWSQ4xQqVMheeumlQy5fsmSJ/fjjj1awYEHLyRYtWmQdO3a0u+66y6688kqrVatWulu6WqE99thjdvbZZ9uIESPsH//4hzVq1Mi9f19//XVUkBk6dKj5HGTU/ngHGb13V1xxhZUsWfKQ6+6//34XJKdMmWIDBgywX375xdq2bWtvvPGGHaveomuuucYuueQSW79+vfXt29fGjx/vgmuVKlVs8ODB1rlzZ/OBXod6bmJ9r4F8vAXIabSymD59uo0ePdry5fv/H3H9CDZu3DjDruysriz27t1ryWTr1q1WqlSpDG83e/ZsW7VqlU2dOtX+7//+L+o6bfkm2+tKNnrvVq9e7Xo2Yrn44outSZMm4fO9e/d2vSLqxYlHj2Dos6fgHsvw4cNd75B66NRG9QyFqMft559/diHrSJ7jWNHn+cILL3Sv59prr01oW5B86JFBjtO9e3f77bffbMGCBeHL9GP873//+5AVdohqW5o3b+6GVgoXLuwCj26fllYGGkbQyv/UU091vTvz5s2L+ZgayurTp4/rzp85c2a4F0Q9AzVr1nQrBz1fixYtotqanu+//966du3qhgaKFCliTZs2tblz5x4ypKHnHTt2bHhYIz3fffed+3vWWWcdcp3aVqJEiXANix4v9PojH/edd95x/9ffWDVDalPa8KRhLD2+/s6aNSvdFahqe/Qe67YKADfccIP98ccfUbdTbY1CgYYSzzjjDHfbE044IWoFrTbofRMN74TaH2rzxx9/bG3atLFy5cq5ZV+jRo1MrSz1WrRs1auV2ZWxHj8yXB+tz96uXbvs0UcfdbdTr1Gsz0HlypXtnnvuyfRzZKedp5xyilsmuu3SpUtjtnXbtm3uM6b3Rz1b6n1R+9O64IIL3HL+/fffYz4Oci96ZJDjaOXWrFkzt+WrrWJRbcL27dvdMIB6atIaNWqU64Lv0aOHCz2vvPKKW/lpGKBdu3aHDN1MmzbN/Vhr5RerUPXAgQNuZfjqq6+6lXXoMVSnMWzYMLvuuuvcilc1ClqRrly50v1QH66AVysR/cDfeuutbmUyefJk12atTDREoBWqhjKuuuoq91hXX331Yd+n6tWru79a6WuYIb3QowChehmFLT1+dr399tvWpUsXq1OnjnsPFDa10jr++ONjPqcCiK7X6123bp2NGTPG9YL897//dXUTId9++60rblaPR8+ePe25555zK0atPLUy1vuix9By19BZ7dq13f30V71X2tIvX768DRw40K1MFcJCwfNw3n//fRfGItsSSZ839f4pWOp5nnrqKVeTpOG+o/nZE63wFRA0vJg3b94MX0tmniMr7dQwrj77et8VhlSoq1qtDz/80L1nkbp16+bCoz4T+h4888wzrqZIQSySlqfeS73vObnGDdkQADnEpEmTAn2kP/roo2DMmDFB8eLFg127drnrunbtGpx33nnu/9WrVw/atWsXdd/Q7UL27t0b1K1bN2jVqlXU5Xr8lJSUYM2aNVGXr1u3zl332GOPBfv27Qsuv/zyoHDhwsH8+fOjbnfaaacd8tyZ0b9/f/f47777bviyP//8M6hRo0aQmpoaHDhwIKqN/fr1y/Ax9ZpPOeUUd3u9J7169QqeffbZYMuWLYfcVo8X6+di8eLF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WrSonXnmma77EseeVkT6IdNJO4UcOHCgO06WdhYpWlm2atXKhVX12PTp08d9NtLSAVXLly/vdoV+4403prvyQ/b17dvXbaF/+OGH1qVLFzv55JPt1FNPdXsp/+CDD8K3+/XXX933rUiRIlazZk17/fXXw9cdOHDAevfubTVq1HDL9JRTTrFRo0bFHC586KGH3LFodJtY0g4t6XPTrVs391tQpkwZ69ixo1sJ48i+m/qdbNSokf3jH/+w1157zYWa0O/xiBEjrF69eu53VL0r+oyEvp86zpKWsW4fadasWVa8eHHbtWtXzKGlN9980322Chcu7MJTbl6GBBnPTZs2zWrVquV+xK688krXpZnZXQPNnTvX/ZC2bdvWVq1a5bb0dRiIEO2EUMNWr7zyihvG6Nq1q9v6+Oabb47iK0JG9AP44osv2kknneRCiw7Z0aZNGytdurR99NFHNn36dPvPf/5zyE4ktXy//PJLF0ZffvllmzlzZswjxSP7dIBa9b6o50UrrbQiNyT03itQ6Lul72CPHj3c/UXDEscff7xbll988YXbs7lWkPq+p12ma9eutQULFtgbb7yRYfv27dvnPitaQb777rv23//+14oVK+a+14Ta+NFGxWmnnea+Y5KSkmKjR4+2NWvW2OTJk11v3YABA9x12qhQ781LL70U9RhTp051QVVBNy2F0UsvvdQNV37yySd23XXXuY2bXEs7xIO/mjdvHowcOdL9f9++fUG5cuWCxYsXu/P6q0X8xx9/uPOTJk0KSpYsGb5vs2bNgh49esR83PXr1wd58+YNfvrpp6jLzz///GDQoEFH8RUhrZ49e7plUbRoUXfSMq1cuXKwYsUKd/2ECROC0qVLB3/99Vf4PnPnzg1SUlKCzZs3hx+jTJkywc6dO8O3GTduXFCsWLHgwIEDvOlxsnz5crd8Zs6cedjb6TaDBw8On9ey02VvvfVWuvfp169f0KVLl/B5LdOKFSsGe/bsibpd9erVgyeffDLquWbNmuX+/8ILLwSnnHJKcPDgwfD1un/hwoWD+fPnZ/HVQsugY8eOMd+Iyy+/PKhdu3bM66ZPnx6ULVs2fF7LR9/F0Pdz+/btQaFChcKfh3Xr1rnluGrVKndev8F16tSJesx77rkn6vc+N6FHxmPaElP3dffu3d15jZ+qoFc1M5mhJH/++efHvE5DFereVteltthCpyVLlth3330X19eBjKnrWMtLJy1zbVWrgHP9+vWul0Vbf5E9AGeddZbbqtdnJES3idy6a9asmevd0dYd4iMrO0qvX79++P9adtoy37p1a/iysWPHulobDQXquzdhwgTbsGFD1GNouKJAgQKZfs7Vq1fbt99+63pkQt9pDS/t3r2b7/VR+CxoOEjUQ6rfWg0/6b2/6qqr7LfffnPDRqIeORULh4YXZ8yY4T4PrVu3jvnY+s5rqD9Ss2bNLLeicshjCiwqJtP4eOSXR2O2Y8aMyfD+GltNj1ZwKjBbsWKF+xtJP344trSi01BSyDPPPOMObz9x4kQWRRJRrYtWXl999VWGt9WKK5LuF5rpouFc1ac98cQTbgWllZ8Kh5cvXx51n1jDV4ej77XCkYYt0lJgQvwobKjGSbUrGjpSHaPqmRQc33vvPVcDpeE8bVwojF522WVueOmKK65wf7VRSnFv5tAj4ykFmClTprgfutCWuk7a4lKwUQ1EZrYI05sO2rBhQ9cjoy1ErUAjTypsQ2Jppadx97///ttq167tlrtqZUJU+6DrIwtAdRvdPkSFpwqlKj5EfGglpd4y9aZELo+QzO7jQ8uvefPmrihU30V97+LRE6piVNW4afZi2u+1gjHiQzUw6tVWsbc2BhVQ9VvdtGlT18sda3apaqRUX6U6Gt1f59Oj77x6ZiN9EFFIntsQZDylwr4//vjDpXrtWyDypC9PZoaXdPRrBR791daDvniPPvqou05fNn2Rrr76alewtm7dOvfFGTZsmCsSxrGlGWTaN4lOWlaabq+taxX7aTlp1lnPnj3t888/t8WLF7vr1X2t/VqEaOtPnxcVj2rGg5a7CoIVeBA/CjHaCFDhvIYIFBy0zFTsmdnuf/XsfPzxxzZ//ny376d7773XFXIfKX1WNDtRM5VU7KvvtYq/b731Vvvxxx+P+PFz83fzp59+spUrV9rDDz/s3l/1wuj3UyFRRdZPPfWUff/99/bCCy/Y+PHjD3mcc845x20kahmpJyft0FEkzTjU5+ruu+92w8fqwTncjNUcL9FFOsie9u3bB23btj1sweGoUaMOW+wrM2bMCBo0aBAUKFDAFQpfeuml4ev27t0bDBkyJEhNTQ3y58/vCkw7d+4cfPrppyy2Y0gFhVqOoVPx4sWD008/Pfj3v/8dvo2WyXnnnecKBFXUe/311wd//vnnIUWJWp4qMlRhoW6ze/duluVRsGnTJlecq8JbfbeOO+644JJLLgkX4kcW4Ibou6nvqGi59OrVy11WqlSp4KabbgoGDhwYnHbaaYcs07QOV+wrP//8c3D11Ve773vBggWDE044wX0WVGCK7H838+XLF5QvXz5o3bp18Nxzz0UV0Y8YMcL9fqqouk2bNsGUKVNiFuYOGDDAXa7vaaS0xb4yZ86c4KSTTnLL8Oyzz3bPmVuLffPon0SHKQAAgOygTxkAAHiLIAMAALxFkAEAAN4iyAAAAG8RZAAAgLcIMgAAwFsEGQAA4C2CDIBj5txzz7X+/fvzjgOIG4IMkIv98ssv7mB21apVcwcb1S7SdawgHesn8rhOs2fPtmTVq1cv69SpU6Zup9fyyCOPRF2u1xY6SjEA/xBkgFxMx+VatWqVTZ482R3T5/XXX3e9Jr/99pvlRDomlY4npuOUAcgZCDJALqUjMevAgVqxn3feeVa9enV3oMNBgwbZJZdc4m6Tmprq/nbu3Nn1WoTOx+oF0ZCRQlCIjv6sg+bpCNuVK1d2R/+NdcC9u+66y4477jgrWrSoO1CeDmIYogPhlSpVyh08UUf81WNddNFF9vPPP7vr//nPf7oQ9tprr7n26RR5/7Rat27tep108NP0KMR1797dtalIkSJWr169Q44mr9epA3PqNZcuXdodnHPixInuNV9zzTVWvHhxd7DAt956K+p+OqjnxRdf7F6H7qMDe/7666/ptgVAxggyQC6llalOGlpRoIgldMTlSZMmufCQlSMw68i8S5YscSHj7bffdgFDRweOpKNvL1u2zF555RX79NNPrWvXri6o6Mi+Ibt27bLHH3/cHTV46dKltmHDBhd+RH+7desWDjc6NW/ePN025c2b1x2dWEciTu9oz7t377bGjRu7o7wrePTp08cFDh39PZIClI4krcsVajREp/br+fU6L7zwQnc/tT8UHFu1amUNGzZ0R7aeN2+ebdmyxbUfwBFI9FErASSOjqBdunRpd9Ts5s2bB4MGDQpWr14ddZtYR2qOdeTl2267LWjZsqX7v468raM+T5s2LXz9b7/95o7+q9vJ+vXrg7x58wY//fRT1OOcf/75rh2io0Hr+b/99tvw9WPHjg0qVqx42LbEEnm7pk2bBtdee637v15bRj+F7dq1C+68887web3OFi1ahM/v378/KFq0aHDVVVdFHWVaj7ts2TJ3/oEHHgguvPDCqMfduHGju83atWszbD+A2OiRAXJ5jcymTZtcbYx6NdRr0qhRIzekcyS+++4727t3rxsqCilTpoydcsop4fOfffaZHThwwE4++eRw75BO6sXR/UM0vHPiiSeGz2uYauvWrUfUPg2nqUflyy+/POQ6temBBx5wQ0pqs9qkoS31BEWqX79+VE9P2bJl3X1CNHQkobauXr3aFi9eHPVaa9WqFX6/AGRPvmzeD0AOKoC94IIL3Onee++16667zu677z5XB5OelJQUdWFEXbZv374sPe9ff/3lAsCKFSvc30hayYfkz58/6jrVwaR97qw655xz3Ows1QOlfZ2PPfaYjRo1ykaOHOmCiWp3VAujYBYpVrsiLwvNhDp48GD49Xbo0MGFqLQUzgBkD0EGQJQ6depETbfWylm9FJHKly/v6kciffLJJ+EVuXpQ9P/ly5e7qd2imUKaGdWyZUt3XrUielz1WJx99tnZXgoFChQ4pH2ZoWnYDRo0iOolEk0979ixo1155ZXhIKJ26305EurpmjFjhiuYzpePn14gXhhaAnIpzc5R8emLL77oCm3XrVtn06dPt+HDh7sVeYhWvAsXLrTNmzeHpy3rfipYnTJliivMVQ9OZLBRj0rv3r1dwe+iRYvcder5UE9OiIaUevTo4WY2zZw50z2/Cmc1o0iFtpml9qn9a9eudTOAMtszpN4WPf/o0aOjLq9Zs6YtWLDA3n//fTf0dMMNN7ii3CPVr18/+/33392MKBVNazhJQ1aa5ZSdIAbgfwgyQC6lsKEalieffNINtdStW9cNLV1//fU2ZsyY8O00bVor9qpVq7peFNGwjG47YMAAO/300+3PP/90gSTtEI16WjScomnPLVq0cLOBImk2lO535513up4RTenWSj7Ui5MZaq/u26RJE9dTFLkzv4zcf//94aGfkMGDB7veE71GTbPWdO3M7HAvI1WqVHFtU2jRjCYFKQ1ZaXp5ZMADkDV5VPGbxfsAAAAkBTYDAACAtwgyAADAWwQZAADgLYIMAADwFkEGAAB4iyADAAC8RZABAADeIsgAAABvEWQAAIC3CDIAAMBbBBkAAOAtggwAADBf/T+ExzrgMHjQ4QAAAABJRU5ErkJggg==",
      "text/plain": [
       "<Figure size 640x480 with 1 Axes>"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "plt.figure()\n",
    "plt.bar(df[\"name\"], df[\"marks\"])\n",
    "plt.xlabel(\"Student Name\")\n",
    "plt.ylabel(\"Marks\")\n",
    "plt.title(\"Marks of Students (Bar Graph)\")\n",
    "plt.show()\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 44,
   "id": "5300d615-a4e9-4873-9be2-284ab874b321",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": "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MlNJBvvKb5oMPH/77bdx9erVx3590u536dq1azh69CimT5+uvl9phZFjlwSpMsj7q6++QlhYGH7++Wd89913D7xOmzZt1Am67CPSkpOz6ygrmW0p+/UHH3ygus6lBedhs4UfSW/BunXrpn/22WcfOuhu7ty5Dx3sK1asWKFv0KCB3t7eXg0U7tOnT+Z9qamp+gkTJuj9/f31dnZ2aoBn79699SdOnCjmT0fGNqhO9iPDxc3NTd+0aVP9H3/8kfkY2SfatWunBsnJoN5XXnlFf+/evWyvIQPzZH+SgXYyuE4ek5ycrNGnouJy/fp1NThXBt7K70qFChX0PXr0yJyEkHUAroH8Lsnvk5B9YsiQIeo2T09P/euvv67/8MMP9U888cQjB3o+bLCvuHHjhn7QoEHqt87BwUFftWpVtR/KAE8y3d8lW1tbvbe3t75Dhw76H3/8MdsEglmzZqljlwzq7ty5s/6nn37KdWDumDFj1O3yG5VVzsG+Yt26dfrq1aurfah169bqPQs72NdK/il8GERERESkHbZHExERkcliIENEREQmi4EMERERmSwGMkRERGSyGMgQERGRyWIgQ0RERCaLgQwRERGZLAYyRFRinnrqKbz77ruscSIqMgxkiCzYrVu31GJwlSpVUgulSopxWetH1urJuibU6tWrYayGDBmCXr165etx8lk+/fTTbLfLZzOs8ktEpoeBDJEFkzXFjh07hiVLlqg1edauXataTaKjo2GOZD0rWQtN1lgjIvPAQIbIQslKyrLwnxzY27Vrh8qVK6uFCseOHYsePXqox/j7+6u/vXv3Vq0Whuu5tYJIl5EEQQayerMsOierc5cvX16tnpvbgnWjR49GhQoV4OLiohaak0UIDWQhOU9PT7X4oayYK6/1zDPP4MaNG+r+SZMmqSBszZo1qnxyyfr8nDp06KBanWTh1rxIEDdgwABVJmdnZwQGBqqFYbOSzymLespnLlWqlFrYc+HCheozDx06FG5ubmqxvb/++ivb82RB0C5duqjPIc+RRUFv376dZ1mI6NEYyBBZKDmYykW6ViSgyI1hxeRFixap4KEgKyjLyra7du1SQcbmzZtVgCGr62YlK3cHBwfjP//5D06cOIF+/fqpQEVWxjVITEzEF198oVbd3b17N65cuaKCHyF/n3/++czgRi5BQUF5lsnGxkat7isr+ea1WnNycjIaN26sVqiXwGPEiBEq4JCV67OSAEpWgpbbJaiRLjopv7y/fM5OnTqp50n5DYFj+/bt0bBhQ7Uy9caNG3Hz5k1VfiJ6DIVZMZOIzIOsvl2qVCm14nZQUJB+7Nix+uPHj2d7TG4rLee2cvI777yjb9u2rdqWVbtl1eZly5Zl3h8dHa1Wz5XHicuXL+ttbGz0165dy/Y6Tz/9tCqHkNWc5f1DQ0Mz7//mm2/0Pj4+Dy1LbrI+rkWLFvqXX35Zbctne9RPYdeuXfXvv/9+5nX5nK1atcq8np6erndxcdG/9NJL2VaJltcNDg5W16dMmaLv1KlTtteNiIhQjwkJCXlk+Ykod2yRIbLwMTLXr19XY2OkVUNaTRo1aqS6dB7HxYsXkZqaqrqKDLy8vFCrVq3M6ydPnkRGRgZq1qyZ2TokF2nFkecbSPdOtWrVMq9LN1VUVNRjlU+606RF5ezZsw/cJ2WaMmWK6lKSMkuZpGtLWoKyql+/fraWntKlS6vnGEjXkTCU9fjx49ixY0e2z1q7du3M+iKiwrEt5POIyIwGwHbs2FFdxo8fj+HDh2PixIlqHExerK2tpQkj221paWkFet/4+HgVABw5ckT9zUoO8gZ2dnbZ7pNxMDnfu6DatGmjZmfJeKCcn/Pzzz/H3LlzMWfOHBWYyNgdGQsjgVlWuZUr622GmVA6nS7z83bv3l0FUTlJcEZEhcNAhoiyqVu3brbp1nJwllaKrLy9vdX4kaz++eefzAO5tKDI9oEDB9TUbiEzhWRmVNu2bdV1GSsirystFq1bty70t2Bvb/9A+fJDpmE3aNAgWyuRkKnnPXv2xIsvvpgZiEi5pV4eh7R0rVixQg2YtrXlTy9RUWHXEpGFktk5Mvj0l19+UQNtw8PDsXz5csycOVMdyA3kwLtt2zZERkZmTluW58mA1Z9++kkNzJUWnKyBjbSoDBs2TA343b59u7pPWj6kJcdAupQGDhyoZjatXLlSvb8MnJUZRTLQNr+kfFL+kJAQNQMovy1D0toi7z9v3rxst9eoUQNbtmzB33//rbqeXn31VTUo93GNHDkSd+7cUTOiZNC0dCdJl5XMcipMIEZE9zGQIbJQEmzIGJbZs2errpZ69eqprqVXXnkFX3/9debjZNq0HNj9/PxUK4qQbhl57JgxY9C0aVPcu3dPBSQ5u2ikpUW6U2Tac6tWrdRsoKxkNpQ87/3331ctIzKlWw7yhlac/JDyynObNGmiWoqyJvN7lMmTJ2d2/Rh8/PHHqvVEPqNMs5bp2vlJuPcovr6+qmwStMiMJgmkpMtKppdnDfCIqGCsZMRvAZ9DREREZBR4GkBEREQmi4EMERERmSwGMkRERGSyGMgQERGRyWIgQ0RERCaLgQwRERGZLAYyREREZLIYyBAREZHJYiBDREREJouBDBEREZksBjJERERkshjIEBEREUzV/wNh4Swf53pfswAAAABJRU5ErkJggg==",
      "text/plain": [
       "<Figure size 640x480 with 1 Axes>"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "plt.figure()\n",
    "sns.lineplot(x=\"name\", y=\"marks\", data=df, marker=\"o\")\n",
    "plt.xlabel(\"Student Name\")\n",
    "plt.ylabel(\"Marks\")\n",
    "plt.title(\"Marks of Students (Line Graph)\")\n",
    "plt.show()\n"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "3e770413-9911-44e1-aff5-841550fe3661",
   "metadata": {},
   "outputs": [],
   "source": []
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3 (ipykernel)",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.14.0"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}
