# Indonesia_Covid19_With_Plotly
Data Visualisation Covid19 in Indonesia On Map 

You can used excel file to process the data if connection to url json file is invalid

import glob
#Membaca semua data kemudian menggabungkannya menjadi satu
Data_Covid = pd.DataFrame(columns=['tanggal', 'KASUS', 'MENINGGAL', 'SEMBUH', 'DIRAWAT_OR_ISOLASI',
       'AKUMULASI_KASUS', 'AKUMULASI_SEMBUH', 'AKUMULASI_MENINGGAL',
       'AKUMULASI_DIRAWAT_OR_ISOLASI','Propinsi'])
files = glob.glob(r'DataCovid*.xlsx')
for f in files:
    print(f)
    Data = pd.read_excel(f'{f}')
    Data_Covid = pd.concat([Data,Data_Covid])
    print(Data_Covid.shape)
