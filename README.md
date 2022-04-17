# Thesis_Remaining_Useful_Life_Prediction
My thesis is inspired by Prognostics and Health Management (PHM) problem of industrial assets, which is an important topic in industry for predicting state of assets to avoid downtime and failures.
Dataset: NASA Turbofan Jet Engine Data Set from Kaggle (https://www.kaggle.com/datasets/behrad3d/nasa-cmaps), including 4 different settings: FD001, FD002, FD003, and FD004.

In this thesis, I used the FD001 setting and started from Vanila-LSTM to predict RUL. In order to get a better result, I tried many different architecture such as: LSTM + Attetion, BiLSTM + Attention, CNN + LSTM, CNN + LSTM + Attention, ResNet + LSTM, ...

From my experience, Conv1D + LSTM + Attention Architecture gives out the best performance in term of both accuracy and speed.

In this architecture, Conv1D layers extract the significant features from the time series. After that LSTM layers use extracted features as the input. The output from LSTM is fed into a custom attention layer in order to improve the result. 

<img width="1224" alt="Screen Shot 2022-03-07 at 21 43 57" src="https://user-images.githubusercontent.com/50269219/163381841-19865bdf-590f-46ef-bf30-3bd6acd46b32.png">

<img width="749" alt="Screen Shot 2022-03-05 at 10 29 52" src="https://user-images.githubusercontent.com/50269219/163381852-a21b3ad9-2df8-4b4c-9b3a-2217c20b59cf.png">

