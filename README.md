

| Iter | Rank | Score       | Model               | Notes                                                              |
| ---- | ---- | ----------- | ------------------- | ------------------------------------------------------------------ |
| 1    |      | 20741.14377 | Reg Lineaire Simple |                                                                    |
| 2    |      | 15518.77645 |                     |                                                                    |
| 3    | 218  | 14359.96800 | XGBoost             | hyperparams optimization                                           |
| 4    | 187  | 14086.14931 | XGBoost             | log transformation + CV optimization                               |
| 5    |      |             |                     |                                                                    |
| 6    |      | 14302.01915 | XGBoost             | Feature Engineering sur les var categ ordinal et les var annuelles |
| 7    |  145    | 13606.22819 | Ensemble Learning 0.80CatBoost + 0.20XGBoost             | Optuna pour rechercher les params
| 8    |  125    | 13547.14667 | Ensemble Learning 0.80CatBoost + 0.20XGBoost             | Austement des params de Optuna |











best_params_cat
iterations          learning_rate'          depth       eval_metric (RMSE)
6706               0.009963790473138256    6            1.1267834617007506


Optuna_catb
1
# # best_params_cat = {
# #     'iterations': 6706,
# #     'learning_rate': 0.009963790473138256,
# #     'depth': 6,
# #     'eval_metric':'RMSE',
# # }
# # 1.1256611748229717

2
# best_params_cat = {
#     'iterations': 6623,
#     'learning_rate': 0.01711,
#     'depth': 5,
#     'eval_metric':'RMSE',
# }


3
best_params_cat
{
    'iterations': 7854,
    'learning_rate': 0.006112041297559089, 
    'depth': 4,
    'eval_metric':'RMSE',
}




Optuna_xgb
1
# # best_params_xgb = {
# #     'n_estimators': 4231,
# #     'learning_rate': 0.005736487269056319,
# #     'colsample_bytree': 0.22253547154828462,
# #     'subsample': 0.6290867610448271,
# #     'min_child_weight': 2,
# # }
# # 1.1267834617007506

2
# best_params_xgb = {
#     'n_estimators': 6696,
#     'learning_rate': 0.00630,
#     'colsample_bytree': 0.22301,
#     'subsample': 0.45878,
#     'min_child_weight': 3,
# }





1.1278363711240071