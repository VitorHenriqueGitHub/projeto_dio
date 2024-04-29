# projeto_dio
projeto azure da dio
Eu inicialmente precisei criar uma conta na azure, inicialmente, eu infelizmente não havia conseguido criar uma conta seguindo o passo a passo da instrututora do curso na DIO, por isso para resolver o problema precisei criar uma conta da azure utilizando meu email institucional, assim me cadastrando na azure for students, uma vez criada essa conta na azure for students, eu consegui acessar os workshops da azure

Após isto precisei ver todas as video-aulas do curso da microsoft para compreender como proseguir no desafio

Agora que eu finalizei todas as video-aulas estou pronto para começar o desafio.
primeiro de tudo precisei acessar o estudio de criação do azure machine learning, onde eu criei um workshop/espaço de trabalho, no qual seu nomei o projeto como "projeto_entrega", uma vez criado eu o acessei. Assim, eu acessei o ML altomatizado criando logo em seguida um novo trabalho de ML altomatizado.

Agora dentro das configurações basicas eu nomei o projeto, assim como seu novo nome de experimento, avançando para a classificação do tipo de tarefa a ser desempenhada pela IA a denominando como do tipo regressão. A seguir eu criei uma base de dados definindo seu nome, sua classificação e seu tipo como sendo Tabular, como demonstrado na aula 4 do modulo eu determinei a criação de uma ativo de dados por url da web, conectando a ia à url https://aka.ms/bike-rentals, partindo então para as configurações deste arquivo da web, onde eu apenas alterei os Cabeçalhos de coluna como sendo "somente o primeiro arquivo tem cabeçalho", avançando para a criação do ativo de dados clicando no botão "criar", uma vez que a base de dados foi criada, eu esperei ela ficar pronta e a selecionei, a seguir cliquei em "avançar" determinando que a coluna de destino seja "rentals(integer)". Uma vez feito isto eu alterei as as definições de configurações adicionais, desmarcando todas as 3 opções, e apenas permitindo os modelos RandomForest e LightGBM.

Agora chegou o momento de definir os limites onde eu defini o Máximo de avaliações, Máximo de avaliações simultâneas, Máximo de nós como sendo igual a 3, o Limite de pontuação da métrica como 0.085, e por fim o Tempo limite do experimento(minutos) e Tempo limite de iteração(minutos) como sendo de 15 minutos, apenas permitindo o encerramento entecipado. 

Feito isto eu defini que o tipo de validação dos dados como sendo de "divisão de validação de treinamento", e deixando a validação percentual de dados como 10, uma vez finalizados as configurações de tarefas, a computação eu tive como preferencia deixar como a padrão, isso é, eu deixei sem servidor, os tipos de maquinas como: CPU e dedicado, e quanto a seu tamanho permiti que fosse: Standard_DS3_v2 (4 núcleo(s), 14GB de RAM, 28 GB de armazenamento, $0.23/hr), tendo um número de instancias de "1" por fim enviando o projeto, o qual eu esperei terminar as execuções para realizar testes.

primeiro verificando suas previsões metricas, evidentemente saindo como o previsto, e verificando seus dados, como por exemplo seus pontos de extremidade os quais tambem não deram problemas.

JSON bruto:
"runId": "affable_rail_8tpp33k4cb",
    "runUuid": "09ec7abe-fb41-4985-90d6-41859041dabb",
    "parentRunUuid": null,
    "rootRunUuid": "09ec7abe-fb41-4985-90d6-41859041dabb",
    "target": "Serverless",
    "status": "Running",
    "parentRunId": null,
    "dataContainerId": "dcid.affable_rail_8tpp33k4cb",
    "createdTimeUtc": "2024-04-29T19:38:35.8696934+00:00",
    "startTimeUtc": "2024-04-29T19:38:49.098Z",
    "endTimeUtc": null,
    "error": null,
    "warnings": null,
    "tags": {
        "model_explain_run": "best_run",
        "automl_best_child_run_id": "entrega_dio_2",
        "_aml_system_automl_mltable_data_json": "{\"Type\":\"MLTable\",\"TrainData\":{\"Uri\":\"azureml://locations/eastus2/workspaces/4145468c-fee4-4f97-b160-85ca0e8e8b73/data/previsao_aluguel_de_bicicletas/versions/1\",\"ResolvedUri\":null,\"AssetId\":null},\"TestData\":null,\"ValidData\":null}",
        "_aml_system_automl_run_workspace_id": "4145468c-fee4-4f97-b160-85ca0e8e8b73",
        "_aml_system_azureml.automlComponent": "AutoML"
    },
    "properties": {
        "num_iterations": "3",
        "training_type": "TrainFull",
        "acquisition_function": "EI",
        "primary_metric": "normalized_root_mean_squared_error",
        "train_split": "0",
        "acquisition_parameter": "0",
        "num_cross_validation": "",
        "target": "Serverless",
        "AMLSettingsJsonString": "{\"is_subgraph_orchestration\":false,\"is_automode\":true,\"path\":\"./sample_projects/\",\"subscription_id\":\"c4725101-1466-43fb-a6f7-8ffb9fc2033e\",\"resource_group\":\"vitinho.almei-rg\",\"workspace_name\":\"projeto-entrega\",\"compute_target\":\"Serverless\",\"iterations\":3,\"primary_metric\":\"normalized_root_mean_squared_error\",\"task_type\":\"regression\",\"IsImageTask\":false,\"IsTextDNNTask\":false,\"validation_size\":0.1,\"n_cross_validations\":null,\"preprocess\":true,\"is_timeseries\":false,\"time_column_name\":null,\"grain_column_names\":null,\"max_cores_per_iteration\":-1,\"max_concurrent_iterations\":3,\"max_nodes\":1,\"iteration_timeout_minutes\":15,\"enforce_time_on_windows\":false,\"experiment_timeout_minutes\":15,\"exit_score\":\"NaN\",\"experiment_exit_score\":0.085,\"whitelist_models\":[\"RandomForest\",\"LightGBM\"],\"blacklist_models\":null,\"blacklist_algos\":[\"TensorFlowDNN\",\"TensorFlowLinearRegressor\"],\"auto_blacklist\":false,\"blacklist_samples_reached\":false,\"exclude_nan_labels\":false,\"verbosity\":20,\"model_explainability\":false,\"enable_onnx_compatible_models\":false,\"enable_feature_sweeping\":false,\"send_telemetry\":true,\"enable_early_stopping\":true,\"early_stopping_n_iters\":20,\"distributed_dnn_max_node_check\":false,\"enable_distributed_featurization\":true,\"enable_distributed_dnn_training\":true,\"enable_distributed_dnn_training_ort_ds\":false,\"ensemble_iterations\":3,\"enable_tf\":false,\"enable_cache\":false,\"enable_subsampling\":false,\"metric_operation\":\"minimize\",\"enable_streaming\":false,\"use_incremental_learning_override\":false,\"force_streaming\":false,\"enable_dnn\":false,\"is_gpu_tmp\":false,\"enable_run_restructure\":false,\"featurization\":\"auto\",\"vm_type\":\"Standard_DS3_v2\",\"vm_priority\":\"dedicated\",\"label_column_name\":\"rentals\",\"weight_column_name\":null,\"miro_flight\":\"default\",\"many_models\":false,\"many_models_process_count_per_node\":0,\"automl_many_models_scenario\":null,\"enable_batch_run\":true,\"save_mlflow\":true,\"track_child_runs\":true,\"test_include_predictions_only\":false,\"enable_mltable_quick_profile\":\"True\",\"has_multiple_series\":false,\"_enable_future_regressors\":false,\"enable_ensembling\":true,\"enable_stack_ensembling\":false,\"ensemble_download_models_timeout_sec\":300.0,\"stack_meta_learner_train_percentage\":0.2}",
        "DataPrepJsonString": null,
        "EnableSubsampling": "False",
        "runTemplate": "AutoML",
        "azureml.runsource": "automl",
        "_aml_internal_automl_best_rai": "False",
        "ClientType": "Mfe",
        "_aml_system_scenario_identification": "Remote.Parent",
        "PlatformVersion": "DPV2",
        "environment_cpu_name": "AzureML-AutoML",
        "environment_cpu_label": "prod",
        "environment_gpu_name": "AzureML-AutoML-GPU",
        "environment_gpu_label": "prod",
        "root_attribution": "automl",
        "attribution": "AutoML",
        "Orchestrator": "AutoML",
        "CancelUri": "https://eastus2.api.azureml.ms/jasmine/v1.0/subscriptions/c4725101-1466-43fb-a6f7-8ffb9fc2033e/resourceGroups/vitinho.almei-rg/providers/Microsoft.MachineLearningServices/workspaces/projeto-entrega/experimentids/71931ba6-c29c-42d6-982e-68ef2e4b0005/cancel/affable_rail_8tpp33k4cb",
        "mltable_data_json": "{\"Type\":\"MLTable\",\"TrainData\":{\"Uri\":\"azureml://locations/eastus2/workspaces/4145468c-fee4-4f97-b160-85ca0e8e8b73/data/previsao_aluguel_de_bicicletas/versions/1\",\"ResolvedUri\":\"azureml://locations/eastus2/workspaces/4145468c-fee4-4f97-b160-85ca0e8e8b73/data/previsao_aluguel_de_bicicletas/versions/1\",\"AssetId\":\"azureml://locations/eastus2/workspaces/4145468c-fee4-4f97-b160-85ca0e8e8b73/data/previsao_aluguel_de_bicicletas/versions/1\"},\"TestData\":null,\"ValidData\":null}",
        "ClientSdkVersion": null,
        "snapshotId": "00000000-0000-0000-0000-000000000000",
        "SetupRunId": "affable_rail_8tpp33k4cb_setup",
        "SetupRunContainerId": "dcid.affable_rail_8tpp33k4cb_setup"
    },
    "parameters": {},
    "services": {},
    "inputDatasets": null,
    "outputDatasets": [],
    "runDefinition": null,
    "logFiles": {},
    "jobCost": {
        "chargedCpuCoreSeconds": null,
        "chargedCpuMemoryMegabyteSeconds": null,
        "chargedGpuSeconds": null,
        "chargedNodeUtilizationSeconds": null
    },
    "revision": 5,
    "runTypeV2": {
        "orchestrator": "AutoML",
        "traits": [
            "automl",
            "Remote.Parent"
        ],
        "attribution": null,
        "computeType": null
    },
    "settings": {},
    "computeRequest": null,
    "compute": {
        "target": "Serverless",
        "targetType": "AmlCompute",
        "vmSize": "Standard_DS3_v2",
        "instanceType": "Standard_DS3_v2",
        "instanceCount": 1,
        "gpuCount": null,
        "priority": "Dedicated",
        "region": null,
        "armId": null,
        "properties": null
    },
    "createdBy": {
        "userObjectId": "11424135-df6a-4b1c-b1b8-304ce673ca86",
        "userPuId": "1003200372DACD1F",
        "userIdp": "live.com",
        "userAltSecId": "1:live.com:000340012BF3796D",
        "userIss": "https://sts.windows.net/5cbd62e8-b9fe-45e9-a867-aa1dde64371a/",
        "userTenantId": "5cbd62e8-b9fe-45e9-a867-aa1dde64371a",
        "userName": "Vitor Nascimento Almeida",
        "upn": null
    },
    "computeDuration": null,
    "effectiveStartTimeUtc": "2024-04-29T19:38:49.0982775+00:00",
    "runNumber": 1714419515,
    "rootRunId": "affable_rail_8tpp33k4cb",
    "experimentId": "71931ba6-c29c-42d6-982e-68ef2e4b0005",
    "userId": "11424135-df6a-4b1c-b1b8-304ce673ca86",
    "statusRevision": 2,
    "currentComputeTime": "00:00:00",
    "lastStartTimeUtc": "2024-04-29T19:38:49.0982775+00:00",
    "lastModifiedBy": {
        "userObjectId": "11424135-df6a-4b1c-b1b8-304ce673ca86",
        "userPuId": "1003200372DACD1F",
        "userIdp": "live.com",
        "userAltSecId": "1:live.com:000340012BF3796D",
        "userIss": "https://sts.windows.net/5cbd62e8-b9fe-45e9-a867-aa1dde64371a/",
        "userTenantId": "5cbd62e8-b9fe-45e9-a867-aa1dde64371a",
        "userName": "Vitor Nascimento Almeida",
        "upn": null
    },
    "lastModifiedUtc": "2024-04-29T19:38:48.1880245+00:00",
    "duration": null,
    "inputs": {
        "training_data": {
            "assetId": "azureml://locations/eastus2/workspaces/4145468c-fee4-4f97-b160-85ca0e8e8b73/data/previsao_aluguel_de_bicicletas/versions/1",
            "type": "MLTable"
        }
    },
    "outputs": null,
    "currentAttemptId": 1
}

