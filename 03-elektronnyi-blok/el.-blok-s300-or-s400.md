# 🔌 Эл. блок S300|S400

## 01. Прикручиваем латунные стойки (важно - сначала стойки - потом заклепки. это значительно ускоряет процесс заклепывания)

{% hint style="info" %}
Латунная стойка М3\*10 -> стальное основание -> гайка М3

Для S400 стойки М3\*40
{% endhint %}

<figure><img src="../.gitbook/assets/изображение (144).png" alt="" width="375"><figcaption></figcaption></figure>

***

## 02. Заклепывание

В стальное основание во все отверстия 5мм заклепываем резьбовые заклепки М3. Кладем основание на стол и клепаем лежачее, так быстрее всего. Заклепки, отмеченные синими стрелками заклепываются опционально, если устанавливается блок питания LRS-150. Если устанавливается блок питания LRS-200 и больше, то заклепки не нужны.&#x20;

<figure><img src="https://lh7-us.googleusercontent.com/buCsXBnnDTriqtQIca7_6SVA4G9UDKNtEQSvDGBytHfTFykTeDgTdd9NhJuV_Zre9wGOUQIxJrJYY6BsOieRaQiYpS0JbFkqxDNaS6ivVeXo9FQ2Nwr0zbvkbEHgWmOB11tGuqqzklH4MYNsVvKMDo4" alt="" width="375"><figcaption></figcaption></figure>

***

## 03. Устанавливаем на основание нейлоновый стойки для плат и фиксаторы проводов

Вставляем стойки, в соответствии с картинкой. В остальные отверстия вставляем фиксаторы проводов, также как на картинке.

Для S400 вместо 20мм стоек ставятся латунные стойки М3\*40

<figure><img src="https://lh7-us.googleusercontent.com/E7sdfa0v9gJXz4-z5mmu5Uh3wXuhhltC_PC9cCFZ70HUL_G9ocSu5XkwX9YCEKuVhIV0HWNl1csEtcEw7HtWRWHF3_JRr1EdsSt_0_SXGiD1FLIImwqJZPbnv8pVDGHqA5lsiv1_2mQ_vcvuByqC5Io" alt="" width="375"><figcaption></figcaption></figure>

***

## 04. Устанавливаем компоненты ЭБ на свои места&#x20;

Устанавливаем правильно перемычки на Fysetc Spider, плату расширения и плату PSU:

[Подробнее о нашей электронике...](https://drive.google.com/drive/folders/1vKXtVQF18aNQGd_E5halMhSocntERmhk)

Всё, кроме SSR и БП, крепится на нейлоновые стойки-защелки.&#x20;

Блок питания крепится винтами М3\*8 в резьбовые заклепки (в случае с LRS-150) или снизу стального основания винтами M4\*6 через 2мм проставку (!!!) в случае с LRS-200 и больше

SSR крепятся винтами М4\*12. Второй SSR устанавливается только в случае, если принтер с нагреваемой камерой.\
Для S400 HT устанавливаются ТРИ SSR (вводное, стол и камера). Стол и камера – SSR 60-DA, вводное – SSR 25-DA. Реле камеры ставится над вводным реле на латунные стойки М4\*35, естественно прикручивать его стоит только после подключения вводного.

RockPi пока не ставим!

Прикручиваем нейлоновые стойки гайка-гайка M4\*35 для вентилятора винтами M4\*6

***

## 05. Подключаем провода в соответствии с картинками и текстовым описанием

Легенда:

<table data-header-hidden data-full-width="false"><thead><tr><th width="215"></th><th width="157"></th><th width="189"></th><th></th></tr></thead><tbody><tr><td>Клемма-вилка</td><td><img src="https://lh7-us.googleusercontent.com/aH4xMuyHLnIH_cPQrHN7NVI9vrYUMNfERcixtkdyADrW_hMRyjfN5Gs_j0PSRvusaOniLOp4wt5SNIeKiuL3LZgsQzBzom_C4r78gxpwr4qhFXOc9hv-99u89H9S35eQM8_77Y1rnRv6UgLsYI4sKtQ" alt=""></td><td>XH2.54-2p</td><td><img src="https://lh7-us.googleusercontent.com/QsMpmPOvqoYEBc9Gr_LnSJ9N5sbBHbGbR6bj1TBHFtbJsURFJRA4zLLlnD8pr7--7d1v2kGPVmKTcW4_4PcqgFT-F7bzjj7CVQPpWS-9vKYJF8li95lax4n6y6MyodKg_zco2ZA1mFpxvDs_9Qnhi28" alt=""></td></tr><tr><td>Клемма-кольцо</td><td><img src="https://lh7-us.googleusercontent.com/Cdd0uWe0T38lzcIrojnakIOz6uXBC3KAxFGqxbC1geGYILDFc2hql6FgGlZJH1ICwgR72Y82tGvWCJ1gChSzSC7o6bDJGWXmgf-FTwoJPXEx2mciTVOkzO4sv8My0eJwph7_C0GSn1yOnkWLbHYF8h0" alt=""></td><td>XH2.54-3p</td><td><img src="https://lh7-us.googleusercontent.com/IT7XHm6opQxUln9AIQcBRboZJDRx466pmiqD0ZIJ6Kj43u6jQtLjmPIvK3zxcWlI27VV9QowBLnDTMTq8N69oSMn_3zlD7ZfQr9dgkvwpQl-vQ3vIFOXJP7DNluKgAPVPOPO4Wz-c0v9XaZulkDHoK4" alt=""></td></tr><tr><td>Клемма 5мм</td><td><img src="https://lh7-us.googleusercontent.com/hJUVJxmpWBjzLv9CI90pNrV6O5JS0PM_oNwduzR5USi0TPuzcjyBvnYOUPq2zctdjq6IMgPqRkbJep8j0j5uBp3H24wA0EqslMsaa_jlRiKTxUqGQNDmPzO4SQSF2_pwCy_9LADjWYAR9MzSA-dbwAI" alt=""></td><td>XH2.54-4p</td><td><img src="https://lh7-us.googleusercontent.com/jnMYfSCgEACN6xoVVE7vBnnd4dqboMnPGZVhfOCgVOI0UNP1cif9SS_gohINRcPUR1Ukk6lEdamFWYLNK6WxR9PfLPoDz5OM106pU13bwD3Zzocx7DIE-4Ds5wzFhwXk37lMD2BlvsJf1dFJIbIr6ls" alt=""></td></tr><tr><td>Клемма 3мм</td><td><img src="https://lh7-us.googleusercontent.com/ZCMY5vgXD8RMhhO8lDfGSjsbXvkgtXCzgaQYOnvSNmnq_HJhO7esX3ih5HkoZEFvGi3K1zhyDu_5W2wbHeqm03jRpsp3tYCona7LR0OLjQlZ2n38c93JpiKdqKqa5_ZAN44JcRAwYztGMN6ZLKWDmTk" alt=""></td><td>DuPont</td><td><img src="https://lh7-us.googleusercontent.com/fUU_pAJ_xOgMASqRC52t7PlnMJG3wudhGysSpJa5jfmBspZNYrzbXF5cUKDG80ZclgLJSLjPv9ViE1OoxzQ6vo5kdbscMZL80MmpLxVpnvweFIgg9SJQi5tMOgRRSrsWl4PDxihHJmhHyeE5mAPMAJ4" alt=""></td></tr><tr><td>НШВИ</td><td><img src="https://lh7-us.googleusercontent.com/BDrfC_khZDn5-pnaQAjWUTzZntO3QLYdDA1Nwk5Sof0kOSuJpJh_534M3u1Dok70iEcJdVGSKqMG3j3kFnTjZNjIheZm2IKzciM4jTcwbQATtZhJunrQzudUOSkGVkP5TyADPpmaZkfPHdy6lMr_XdQ" alt=""></td><td>Двойной НШВИ</td><td><img src="https://lh7-us.googleusercontent.com/jskQoL94blk_8nuubuVCZO7IZ7vhBDAoYwtvpp0PWOMbrnXLxneNN6T1VR111rY_aXchequWDXYOxoutRm1rVggACevNTWEh-B7dy-zTQIaYx4IbFj-vTAm6-mvV61UIgbnYYQQGg5rKRH28hRtHGBY" alt=""></td></tr></tbody></table>

***

### 01. Силовая часть 220v.&#x20;

Провода для S300:     Провода для S400 HT

<table data-header-hidden><thead><tr><th width="123"></th><th width="114"></th><th width="88"></th><th width="103"></th><th></th><th width="53"></th><th width="69"></th><th></th><th></th></tr></thead><tbody><tr><td>Черный 1.5 кв.мм.</td><td>25 см</td><td><img src="https://lh7-us.googleusercontent.com/hJUVJxmpWBjzLv9CI90pNrV6O5JS0PM_oNwduzR5USi0TPuzcjyBvnYOUPq2zctdjq6IMgPqRkbJep8j0j5uBp3H24wA0EqslMsaa_jlRiKTxUqGQNDmPzO4SQSF2_pwCy_9LADjWYAR9MzSA-dbwAI" alt=""></td><td><img src="https://lh7-us.googleusercontent.com/BDrfC_khZDn5-pnaQAjWUTzZntO3QLYdDA1Nwk5Sof0kOSuJpJh_534M3u1Dok70iEcJdVGSKqMG3j3kFnTjZNjIheZm2IKzciM4jTcwbQATtZhJunrQzudUOSkGVkP5TyADPpmaZkfPHdy6lMr_XdQ" alt=""></td><td><br></td><td>Черный 2.5 кв.мм.</td><td>25 см</td><td><img src="https://lh7-us.googleusercontent.com/hJUVJxmpWBjzLv9CI90pNrV6O5JS0PM_oNwduzR5USi0TPuzcjyBvnYOUPq2zctdjq6IMgPqRkbJep8j0j5uBp3H24wA0EqslMsaa_jlRiKTxUqGQNDmPzO4SQSF2_pwCy_9LADjWYAR9MzSA-dbwAI" alt=""></td><td><p><br></p><p><img src="https://lh7-us.googleusercontent.com/jskQoL94blk_8nuubuVCZO7IZ7vhBDAoYwtvpp0PWOMbrnXLxneNN6T1VR111rY_aXchequWDXYOxoutRm1rVggACevNTWEh-B7dy-zTQIaYx4IbFj-vTAm6-mvV61UIgbnYYQQGg5rKRH28hRtHGBY" alt=""></p></td></tr><tr><td>XX см</td><td><img src="https://lh7-us.googleusercontent.com/hJUVJxmpWBjzLv9CI90pNrV6O5JS0PM_oNwduzR5USi0TPuzcjyBvnYOUPq2zctdjq6IMgPqRkbJep8j0j5uBp3H24wA0EqslMsaa_jlRiKTxUqGQNDmPzO4SQSF2_pwCy_9LADjWYAR9MzSA-dbwAI" alt=""></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr><tr><td>Красный 1.5 кв.мм.</td><td>25 см</td><td><p><br></p><p><img src="https://lh7-us.googleusercontent.com/hJUVJxmpWBjzLv9CI90pNrV6O5JS0PM_oNwduzR5USi0TPuzcjyBvnYOUPq2zctdjq6IMgPqRkbJep8j0j5uBp3H24wA0EqslMsaa_jlRiKTxUqGQNDmPzO4SQSF2_pwCy_9LADjWYAR9MzSA-dbwAI" alt=""></p></td><td><img src="https://lh7-us.googleusercontent.com/BDrfC_khZDn5-pnaQAjWUTzZntO3QLYdDA1Nwk5Sof0kOSuJpJh_534M3u1Dok70iEcJdVGSKqMG3j3kFnTjZNjIheZm2IKzciM4jTcwbQATtZhJunrQzudUOSkGVkP5TyADPpmaZkfPHdy6lMr_XdQ" alt=""></td><td><p>Красный 2.5 кв.мм.</p><p>(флажковая клемма через предохранитель)</p></td><td>XX см</td><td><img src="https://lh7-us.googleusercontent.com/hJUVJxmpWBjzLv9CI90pNrV6O5JS0PM_oNwduzR5USi0TPuzcjyBvnYOUPq2zctdjq6IMgPqRkbJep8j0j5uBp3H24wA0EqslMsaa_jlRiKTxUqGQNDmPzO4SQSF2_pwCy_9LADjWYAR9MzSA-dbwAI" alt=""></td><td><img src="https://lh7-us.googleusercontent.com/jskQoL94blk_8nuubuVCZO7IZ7vhBDAoYwtvpp0PWOMbrnXLxneNN6T1VR111rY_aXchequWDXYOxoutRm1rVggACevNTWEh-B7dy-zTQIaYx4IbFj-vTAm6-mvV61UIgbnYYQQGg5rKRH28hRtHGBY" alt=""></td><td></td></tr><tr><td>8 см</td><td><img src="https://lh7-us.googleusercontent.com/aH4xMuyHLnIH_cPQrHN7NVI9vrYUMNfERcixtkdyADrW_hMRyjfN5Gs_j0PSRvusaOniLOp4wt5SNIeKiuL3LZgsQzBzom_C4r78gxpwr4qhFXOc9hv-99u89H9S35eQM8_77Y1rnRv6UgLsYI4sKtQ" alt=""></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr><tr><td>Желтый 1.5 кв.мм.</td><td>25 см</td><td><img src="https://lh7-us.googleusercontent.com/hJUVJxmpWBjzLv9CI90pNrV6O5JS0PM_oNwduzR5USi0TPuzcjyBvnYOUPq2zctdjq6IMgPqRkbJep8j0j5uBp3H24wA0EqslMsaa_jlRiKTxUqGQNDmPzO4SQSF2_pwCy_9LADjWYAR9MzSA-dbwAI" alt=""></td><td><img src="https://lh7-us.googleusercontent.com/jskQoL94blk_8nuubuVCZO7IZ7vhBDAoYwtvpp0PWOMbrnXLxneNN6T1VR111rY_aXchequWDXYOxoutRm1rVggACevNTWEh-B7dy-zTQIaYx4IbFj-vTAm6-mvV61UIgbnYYQQGg5rKRH28hRtHGBY" alt=""></td><td>Желтый 2.5 кв.мм.</td><td>XX см</td><td><img src="https://lh7-us.googleusercontent.com/hJUVJxmpWBjzLv9CI90pNrV6O5JS0PM_oNwduzR5USi0TPuzcjyBvnYOUPq2zctdjq6IMgPqRkbJep8j0j5uBp3H24wA0EqslMsaa_jlRiKTxUqGQNDmPzO4SQSF2_pwCy_9LADjWYAR9MzSA-dbwAI" alt=""></td><td><img src="https://lh7-us.googleusercontent.com/jskQoL94blk_8nuubuVCZO7IZ7vhBDAoYwtvpp0PWOMbrnXLxneNN6T1VR111rY_aXchequWDXYOxoutRm1rVggACevNTWEh-B7dy-zTQIaYx4IbFj-vTAm6-mvV61UIgbnYYQQGg5rKRH28hRtHGBY" alt=""></td><td></td></tr><tr><td>25 см</td><td><img src="https://lh7-us.googleusercontent.com/Cdd0uWe0T38lzcIrojnakIOz6uXBC3KAxFGqxbC1geGYILDFc2hql6FgGlZJH1ICwgR72Y82tGvWCJ1gChSzSC7o6bDJGWXmgf-FTwoJPXEx2mciTVOkzO4sv8My0eJwph7_C0GSn1yOnkWLbHYF8h0" alt=""></td><td>25 см</td><td><img src="https://lh7-us.googleusercontent.com/Cdd0uWe0T38lzcIrojnakIOz6uXBC3KAxFGqxbC1geGYILDFc2hql6FgGlZJH1ICwgR72Y82tGvWCJ1gChSzSC7o6bDJGWXmgf-FTwoJPXEx2mciTVOkzO4sv8My0eJwph7_C0GSn1yOnkWLbHYF8h0" alt=""></td><td></td><td></td><td></td><td></td><td></td></tr><tr><td>Красный 1.5 кв.мм.</td><td>18 см</td><td><img src="https://lh7-us.googleusercontent.com/aH4xMuyHLnIH_cPQrHN7NVI9vrYUMNfERcixtkdyADrW_hMRyjfN5Gs_j0PSRvusaOniLOp4wt5SNIeKiuL3LZgsQzBzom_C4r78gxpwr4qhFXOc9hv-99u89H9S35eQM8_77Y1rnRv6UgLsYI4sKtQ" alt=""></td><td><img src="https://lh7-us.googleusercontent.com/BDrfC_khZDn5-pnaQAjWUTzZntO3QLYdDA1Nwk5Sof0kOSuJpJh_534M3u1Dok70iEcJdVGSKqMG3j3kFnTjZNjIheZm2IKzciM4jTcwbQATtZhJunrQzudUOSkGVkP5TyADPpmaZkfPHdy6lMr_XdQ" alt=""></td><td>Красный 2.5 кв.мм.</td><td>15 см</td><td><img src="https://lh7-us.googleusercontent.com/aH4xMuyHLnIH_cPQrHN7NVI9vrYUMNfERcixtkdyADrW_hMRyjfN5Gs_j0PSRvusaOniLOp4wt5SNIeKiuL3LZgsQzBzom_C4r78gxpwr4qhFXOc9hv-99u89H9S35eQM8_77Y1rnRv6UgLsYI4sKtQ" alt=""></td><td><img src="https://lh7-us.googleusercontent.com/jskQoL94blk_8nuubuVCZO7IZ7vhBDAoYwtvpp0PWOMbrnXLxneNN6T1VR111rY_aXchequWDXYOxoutRm1rVggACevNTWEh-B7dy-zTQIaYx4IbFj-vTAm6-mvV61UIgbnYYQQGg5rKRH28hRtHGBY" alt=""></td><td></td></tr><tr><td>5 см</td><td><img src="https://lh7-us.googleusercontent.com/aH4xMuyHLnIH_cPQrHN7NVI9vrYUMNfERcixtkdyADrW_hMRyjfN5Gs_j0PSRvusaOniLOp4wt5SNIeKiuL3LZgsQzBzom_C4r78gxpwr4qhFXOc9hv-99u89H9S35eQM8_77Y1rnRv6UgLsYI4sKtQ" alt=""></td><td></td><td></td><td></td><td></td><td></td><td></td><td></td></tr><tr><td>Красный 1.5 кв.мм. </td><td>18 см</td><td><img src="https://lh7-us.googleusercontent.com/aH4xMuyHLnIH_cPQrHN7NVI9vrYUMNfERcixtkdyADrW_hMRyjfN5Gs_j0PSRvusaOniLOp4wt5SNIeKiuL3LZgsQzBzom_C4r78gxpwr4qhFXOc9hv-99u89H9S35eQM8_77Y1rnRv6UgLsYI4sKtQ" alt=""></td><td><img src="https://lh7-us.googleusercontent.com/BDrfC_khZDn5-pnaQAjWUTzZntO3QLYdDA1Nwk5Sof0kOSuJpJh_534M3u1Dok70iEcJdVGSKqMG3j3kFnTjZNjIheZm2IKzciM4jTcwbQATtZhJunrQzudUOSkGVkP5TyADPpmaZkfPHdy6lMr_XdQ" alt=""></td><td>Красный 1.5 кв.мм. </td><td>18 см</td><td><img src="https://lh7-us.googleusercontent.com/aH4xMuyHLnIH_cPQrHN7NVI9vrYUMNfERcixtkdyADrW_hMRyjfN5Gs_j0PSRvusaOniLOp4wt5SNIeKiuL3LZgsQzBzom_C4r78gxpwr4qhFXOc9hv-99u89H9S35eQM8_77Y1rnRv6UgLsYI4sKtQ" alt=""></td><td><img src="https://lh7-us.googleusercontent.com/aH4xMuyHLnIH_cPQrHN7NVI9vrYUMNfERcixtkdyADrW_hMRyjfN5Gs_j0PSRvusaOniLOp4wt5SNIeKiuL3LZgsQzBzom_C4r78gxpwr4qhFXOc9hv-99u89H9S35eQM8_77Y1rnRv6UgLsYI4sKtQ" alt=""></td><td></td></tr><tr><td>Желтый 1.5 кв.мм. </td><td>18 см</td><td><img src="https://lh7-us.googleusercontent.com/aH4xMuyHLnIH_cPQrHN7NVI9vrYUMNfERcixtkdyADrW_hMRyjfN5Gs_j0PSRvusaOniLOp4wt5SNIeKiuL3LZgsQzBzom_C4r78gxpwr4qhFXOc9hv-99u89H9S35eQM8_77Y1rnRv6UgLsYI4sKtQ" alt=""></td><td><img src="https://lh7-us.googleusercontent.com/BDrfC_khZDn5-pnaQAjWUTzZntO3QLYdDA1Nwk5Sof0kOSuJpJh_534M3u1Dok70iEcJdVGSKqMG3j3kFnTjZNjIheZm2IKzciM4jTcwbQATtZhJunrQzudUOSkGVkP5TyADPpmaZkfPHdy6lMr_XdQ" alt=""></td><td>Желтый 1.5 кв.мм. </td><td>18 см</td><td><img src="https://lh7-us.googleusercontent.com/aH4xMuyHLnIH_cPQrHN7NVI9vrYUMNfERcixtkdyADrW_hMRyjfN5Gs_j0PSRvusaOniLOp4wt5SNIeKiuL3LZgsQzBzom_C4r78gxpwr4qhFXOc9hv-99u89H9S35eQM8_77Y1rnRv6UgLsYI4sKtQ" alt=""></td><td><img src="https://lh7-us.googleusercontent.com/BDrfC_khZDn5-pnaQAjWUTzZntO3QLYdDA1Nwk5Sof0kOSuJpJh_534M3u1Dok70iEcJdVGSKqMG3j3kFnTjZNjIheZm2IKzciM4jTcwbQATtZhJunrQzudUOSkGVkP5TyADPpmaZkfPHdy6lMr_XdQ" alt=""></td><td></td></tr><tr><td>Черный 1.5 кв.мм. </td><td>18 см</td><td><img src="https://lh7-us.googleusercontent.com/aH4xMuyHLnIH_cPQrHN7NVI9vrYUMNfERcixtkdyADrW_hMRyjfN5Gs_j0PSRvusaOniLOp4wt5SNIeKiuL3LZgsQzBzom_C4r78gxpwr4qhFXOc9hv-99u89H9S35eQM8_77Y1rnRv6UgLsYI4sKtQ" alt=""></td><td><img src="https://lh7-us.googleusercontent.com/BDrfC_khZDn5-pnaQAjWUTzZntO3QLYdDA1Nwk5Sof0kOSuJpJh_534M3u1Dok70iEcJdVGSKqMG3j3kFnTjZNjIheZm2IKzciM4jTcwbQATtZhJunrQzudUOSkGVkP5TyADPpmaZkfPHdy6lMr_XdQ" alt=""></td><td>Черный 1.5 кв.мм. </td><td>18 см</td><td><img src="https://lh7-us.googleusercontent.com/aH4xMuyHLnIH_cPQrHN7NVI9vrYUMNfERcixtkdyADrW_hMRyjfN5Gs_j0PSRvusaOniLOp4wt5SNIeKiuL3LZgsQzBzom_C4r78gxpwr4qhFXOc9hv-99u89H9S35eQM8_77Y1rnRv6UgLsYI4sKtQ" alt=""></td><td><img src="https://lh7-us.googleusercontent.com/BDrfC_khZDn5-pnaQAjWUTzZntO3QLYdDA1Nwk5Sof0kOSuJpJh_534M3u1Dok70iEcJdVGSKqMG3j3kFnTjZNjIheZm2IKzciM4jTcwbQATtZhJunrQzudUOSkGVkP5TyADPpmaZkfPHdy6lMr_XdQ" alt=""></td><td></td></tr><tr><td>Черный 1.5 кв.мм. </td><td>18 см</td><td><img src="https://lh7-us.googleusercontent.com/aH4xMuyHLnIH_cPQrHN7NVI9vrYUMNfERcixtkdyADrW_hMRyjfN5Gs_j0PSRvusaOniLOp4wt5SNIeKiuL3LZgsQzBzom_C4r78gxpwr4qhFXOc9hv-99u89H9S35eQM8_77Y1rnRv6UgLsYI4sKtQ" alt=""></td><td><img src="https://lh7-us.googleusercontent.com/BDrfC_khZDn5-pnaQAjWUTzZntO3QLYdDA1Nwk5Sof0kOSuJpJh_534M3u1Dok70iEcJdVGSKqMG3j3kFnTjZNjIheZm2IKzciM4jTcwbQATtZhJunrQzudUOSkGVkP5TyADPpmaZkfPHdy6lMr_XdQ" alt=""></td><td>Черный 1.5 кв.мм. </td><td>18 см</td><td><img src="https://lh7-us.googleusercontent.com/aH4xMuyHLnIH_cPQrHN7NVI9vrYUMNfERcixtkdyADrW_hMRyjfN5Gs_j0PSRvusaOniLOp4wt5SNIeKiuL3LZgsQzBzom_C4r78gxpwr4qhFXOc9hv-99u89H9S35eQM8_77Y1rnRv6UgLsYI4sKtQ" alt=""></td><td><img src="https://lh7-us.googleusercontent.com/BDrfC_khZDn5-pnaQAjWUTzZntO3QLYdDA1Nwk5Sof0kOSuJpJh_534M3u1Dok70iEcJdVGSKqMG3j3kFnTjZNjIheZm2IKzciM4jTcwbQATtZhJunrQzudUOSkGVkP5TyADPpmaZkfPHdy6lMr_XdQ" alt=""></td><td></td></tr></tbody></table>

Описание:

В зеленые колодки подключаем НШВИ, к SSR и блоку питания подключаем клеммы-вилки. Флажковые клеммы остаются неподключенными – они подключаются на этапе сборки принтера к разъему питания и нагревателю камеры (в случае с S400 HT).

Для S300 показан вариант подключения с блоком питания LRS-150-24. Если устанавливается LRS-200 и больше, то нужно смотреть на название контактов!

***

### Провода для кнопки включения и управление SSR-ами

Провода для S300: Провода для S400

| Шлейф подключения кнопки | 50 см       | ![](https://lh7-us.googleusercontent.com/WKBehLQCwiWdoSWU34baaN4Kr8ofvygmxP_xXYJ_X5Y_pQUT8ftakZudPg8m9thjd3Bju1VLDX3ysa-NWctWtrI5QTlbYiaIG0PHtV20U2w_GWEMg0uETSbRKEcyg5pbCLNkXg0Fzb4HsUpz6mlg1Xw) | ![](https://lh7-us.googleusercontent.com/MN9IWy7i578iMZb7BExDeZZy2nLSO1iM2hrtfYCbbB36yjrejjRvBOvRJ8_42970_RloItzZVhJo7tUE7xs6kT4In31nzQt9nGooa0Xv31n-r-0YXtxJKWQIrtDlsxNQU9SJHbCkOBJrz9YEKEzYlZk) | <p><br></p>                                                                                                                                                                                       | Шлейф подключения кнопки                                                                                                                                                                          | XX см | ![](https://lh7-us.googleusercontent.com/ZCMY5vgXD8RMhhO8lDfGSjsbXvkgtXCzgaQYOnvSNmnq_HJhO7esX3ih5HkoZEFvGi3K1zhyDu_5W2wbHeqm03jRpsp3tYCona7LR0OLjQlZ2n38c93JpiKdqKqa5_ZAN44JcRAwYztGMN6ZLKWDmTk) | ![](https://lh7-us.googleusercontent.com/MN9IWy7i578iMZb7BExDeZZy2nLSO1iM2hrtfYCbbB36yjrejjRvBOvRJ8_42970_RloItzZVhJo7tUE7xs6kT4In31nzQt9nGooa0Xv31n-r-0YXtxJKWQIrtDlsxNQU9SJHbCkOBJrz9YEKEzYlZk) |
| ------------------------ | ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Управление SSR стола     | 17 см       | ![](https://lh7-us.googleusercontent.com/z6g3Gr2KlaLOetfAjHkbtzpBcIocN_dVaZ9qf1ByNO97ubKz4FCfuFCG3IcwLbg2XAWj-rTFbdWtKaVJWaJDpbM3fSkzfzS46yIH6GVUhptAmZO0Su4xVskDQAcEnmYlO6h5xiyFi6Pa4W_yKH8V_k4) | ![](https://lh7-us.googleusercontent.com/z6g3Gr2KlaLOetfAjHkbtzpBcIocN_dVaZ9qf1ByNO97ubKz4FCfuFCG3IcwLbg2XAWj-rTFbdWtKaVJWaJDpbM3fSkzfzS46yIH6GVUhptAmZO0Su4xVskDQAcEnmYlO6h5xiyFi6Pa4W_yKH8V_k4) | <p><br></p>                                                                                                                                                                                       | Управление SSR стола                                                                                                                                                                              | 17 см | ![](https://lh7-us.googleusercontent.com/z6g3Gr2KlaLOetfAjHkbtzpBcIocN_dVaZ9qf1ByNO97ubKz4FCfuFCG3IcwLbg2XAWj-rTFbdWtKaVJWaJDpbM3fSkzfzS46yIH6GVUhptAmZO0Su4xVskDQAcEnmYlO6h5xiyFi6Pa4W_yKH8V_k4) | ![](https://lh7-us.googleusercontent.com/z6g3Gr2KlaLOetfAjHkbtzpBcIocN_dVaZ9qf1ByNO97ubKz4FCfuFCG3IcwLbg2XAWj-rTFbdWtKaVJWaJDpbM3fSkzfzS46yIH6GVUhptAmZO0Su4xVskDQAcEnmYlO6h5xiyFi6Pa4W_yKH8V_k4) |
| Управление SSR камеры    | 20 см       | ![](https://lh7-us.googleusercontent.com/z6g3Gr2KlaLOetfAjHkbtzpBcIocN_dVaZ9qf1ByNO97ubKz4FCfuFCG3IcwLbg2XAWj-rTFbdWtKaVJWaJDpbM3fSkzfzS46yIH6GVUhptAmZO0Su4xVskDQAcEnmYlO6h5xiyFi6Pa4W_yKH8V_k4) | ![](https://lh7-us.googleusercontent.com/z6g3Gr2KlaLOetfAjHkbtzpBcIocN_dVaZ9qf1ByNO97ubKz4FCfuFCG3IcwLbg2XAWj-rTFbdWtKaVJWaJDpbM3fSkzfzS46yIH6GVUhptAmZO0Su4xVskDQAcEnmYlO6h5xiyFi6Pa4W_yKH8V_k4) | <p><br></p>                                                                                                                                                                                       | Управление SSR камеры                                                                                                                                                                             | 20см  | ![](https://lh7-us.googleusercontent.com/z6g3Gr2KlaLOetfAjHkbtzpBcIocN_dVaZ9qf1ByNO97ubKz4FCfuFCG3IcwLbg2XAWj-rTFbdWtKaVJWaJDpbM3fSkzfzS46yIH6GVUhptAmZO0Su4xVskDQAcEnmYlO6h5xiyFi6Pa4W_yKH8V_k4) | ![](https://lh7-us.googleusercontent.com/z6g3Gr2KlaLOetfAjHkbtzpBcIocN_dVaZ9qf1ByNO97ubKz4FCfuFCG3IcwLbg2XAWj-rTFbdWtKaVJWaJDpbM3fSkzfzS46yIH6GVUhptAmZO0Su4xVskDQAcEnmYlO6h5xiyFi6Pa4W_yKH8V_k4) |
| <p><br></p>              | <p><br></p> | Управление SSR вводного                                                                                                                                                                           | XX см                                                                                                                                                                                             | ![](https://lh7-us.googleusercontent.com/QsMpmPOvqoYEBc9Gr_LnSJ9N5sbBHbGbR6bj1TBHFtbJsURFJRA4zLLlnD8pr7--7d1v2kGPVmKTcW4_4PcqgFT-F7bzjj7CVQPpWS-9vKYJF8li95lax4n6y6MyodKg_zco2ZA1mFpxvDs_9Qnhi28) | ![](https://lh7-us.googleusercontent.com/z6g3Gr2KlaLOetfAjHkbtzpBcIocN_dVaZ9qf1ByNO97ubKz4FCfuFCG3IcwLbg2XAWj-rTFbdWtKaVJWaJDpbM3fSkzfzS46yIH6GVUhptAmZO0Su4xVskDQAcEnmYlO6h5xiyFi6Pa4W_yKH8V_k4) |       |                                                                                                                                                                                                   |                                                                                                                                                                                                   |

Описание:

Для S300/S300HT подключаем, как на картинке ниже. То, что пунктиром, подключается только для HT версии.

Для S400 подключаем как на картинке ниже. Для HT версии после подключения вводного реле, сверху прикручиваем реле нагревателя камеры и подключаем как на картинке (пунктиром).

***

### Цепь 24В

\


| <p><br></p> | Черный 1.5 кв.мм                                                                                                                                                                                  | 45 см | ![](https://lh7-us.googleusercontent.com/jskQoL94blk_8nuubuVCZO7IZ7vhBDAoYwtvpp0PWOMbrnXLxneNN6T1VR111rY_aXchequWDXYOxoutRm1rVggACevNTWEh-B7dy-zTQIaYx4IbFj-vTAm6-mvV61UIgbnYYQQGg5rKRH28hRtHGBY) | ![](https://lh7-us.googleusercontent.com/aH4xMuyHLnIH_cPQrHN7NVI9vrYUMNfERcixtkdyADrW_hMRyjfN5Gs_j0PSRvusaOniLOp4wt5SNIeKiuL3LZgsQzBzom_C4r78gxpwr4qhFXOc9hv-99u89H9S35eQM8_77Y1rnRv6UgLsYI4sKtQ) |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 8 см        | ![](https://lh7-us.googleusercontent.com/BDrfC_khZDn5-pnaQAjWUTzZntO3QLYdDA1Nwk5Sof0kOSuJpJh_534M3u1Dok70iEcJdVGSKqMG3j3kFnTjZNjIheZm2IKzciM4jTcwbQATtZhJunrQzudUOSkGVkP5TyADPpmaZkfPHdy6lMr_XdQ) |       |                                                                                                                                                                                                   |                                                                                                                                                                                                   |
| <p><br></p> | Красный 1.5 кв.мм                                                                                                                                                                                 | 45 см | ![](https://lh7-us.googleusercontent.com/jskQoL94blk_8nuubuVCZO7IZ7vhBDAoYwtvpp0PWOMbrnXLxneNN6T1VR111rY_aXchequWDXYOxoutRm1rVggACevNTWEh-B7dy-zTQIaYx4IbFj-vTAm6-mvV61UIgbnYYQQGg5rKRH28hRtHGBY) | ![](https://lh7-us.googleusercontent.com/aH4xMuyHLnIH_cPQrHN7NVI9vrYUMNfERcixtkdyADrW_hMRyjfN5Gs_j0PSRvusaOniLOp4wt5SNIeKiuL3LZgsQzBzom_C4r78gxpwr4qhFXOc9hv-99u89H9S35eQM8_77Y1rnRv6UgLsYI4sKtQ) |
| 8 см        | ![](https://lh7-us.googleusercontent.com/BDrfC_khZDn5-pnaQAjWUTzZntO3QLYdDA1Nwk5Sof0kOSuJpJh_534M3u1Dok70iEcJdVGSKqMG3j3kFnTjZNjIheZm2IKzciM4jTcwbQATtZhJunrQzudUOSkGVkP5TyADPpmaZkfPHdy6lMr_XdQ) |       |                                                                                                                                                                                                   |                                                                                                                                                                                                   |

Описание:

С клемм БП 24В V+ и V- подключаем провода на разъем PWR\_IN Fysetc Spider, соблюдая полярность. Перемычки подключаем к разъему BED\_IN соблюдая полярность. (один конец перемычки и один конец провод питания спайдера обжимаются ДВОЙНЫМ НШВИ, иначе ужасный контакт и обгоревший разъем)

Для S400/S400 HT тоже самое, только другой блок питания, смотрите на наименование клемм блока питания!&#x20;



### Подключаем плату Extension v2.2

\


| <p><br></p> | Шлейф HEAT0 (красно-черный) | ![](https://lh7-us.googleusercontent.com/z6g3Gr2KlaLOetfAjHkbtzpBcIocN_dVaZ9qf1ByNO97ubKz4FCfuFCG3IcwLbg2XAWj-rTFbdWtKaVJWaJDpbM3fSkzfzS46yIH6GVUhptAmZO0Su4xVskDQAcEnmYlO6h5xiyFi6Pa4W_yKH8V_k4) | ![](https://lh7-us.googleusercontent.com/z6g3Gr2KlaLOetfAjHkbtzpBcIocN_dVaZ9qf1ByNO97ubKz4FCfuFCG3IcwLbg2XAWj-rTFbdWtKaVJWaJDpbM3fSkzfzS46yIH6GVUhptAmZO0Su4xVskDQAcEnmYlO6h5xiyFi6Pa4W_yKH8V_k4) |
| ----------- | --------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p><br></p> | Шлейф X-MIN 3pin            | ![](https://lh7-us.googleusercontent.com/nGbtAiurH_FeWrNQSZpJe42BGepzsk12w4a_IsJvbMCPc8cNYq0AGlIz3bwk6tmHMi5Xy0YbXBkEde0Db8x3hid55zsi-i5RNkOp9ju0JkgzqMgsN6-fL0k_WRZgip1FF5Tzuiw2uQiAuHA_HFE-pv8) | ![](https://lh7-us.googleusercontent.com/nGbtAiurH_FeWrNQSZpJe42BGepzsk12w4a_IsJvbMCPc8cNYq0AGlIz3bwk6tmHMi5Xy0YbXBkEde0Db8x3hid55zsi-i5RNkOp9ju0JkgzqMgsN6-fL0k_WRZgip1FF5Tzuiw2uQiAuHA_HFE-pv8) |
| <p><br></p> | Шлейф Z-MIN 3pin            | ![](https://lh7-us.googleusercontent.com/nGbtAiurH_FeWrNQSZpJe42BGepzsk12w4a_IsJvbMCPc8cNYq0AGlIz3bwk6tmHMi5Xy0YbXBkEde0Db8x3hid55zsi-i5RNkOp9ju0JkgzqMgsN6-fL0k_WRZgip1FF5Tzuiw2uQiAuHA_HFE-pv8) | ![](https://lh7-us.googleusercontent.com/nGbtAiurH_FeWrNQSZpJe42BGepzsk12w4a_IsJvbMCPc8cNYq0AGlIz3bwk6tmHMi5Xy0YbXBkEde0Db8x3hid55zsi-i5RNkOp9ju0JkgzqMgsN6-fL0k_WRZgip1FF5Tzuiw2uQiAuHA_HFE-pv8) |
| <p><br></p> | Шлейф FAN5 2pin             | ![](https://lh7-us.googleusercontent.com/3p9WA5cczYXgJpdoEupRBxspQGWz_2sNVaVXMx39AevRctoEAKr39cxtkH7o2j6kejcdPGg2IhCQgS6hN7ViRGOHDCPGuLnSDTV_gIkMakXUuruq5uZI2ymmXudXzWqfVZRKsD5VsTAMikgV2SOi-kE) | ![](https://lh7-us.googleusercontent.com/3p9WA5cczYXgJpdoEupRBxspQGWz_2sNVaVXMx39AevRctoEAKr39cxtkH7o2j6kejcdPGg2IhCQgS6hN7ViRGOHDCPGuLnSDTV_gIkMakXUuruq5uZI2ymmXudXzWqfVZRKsD5VsTAMikgV2SOi-kE) |
| <p><br></p> | Шлейф FAN0 2pin             | ![](https://lh7-us.googleusercontent.com/3p9WA5cczYXgJpdoEupRBxspQGWz_2sNVaVXMx39AevRctoEAKr39cxtkH7o2j6kejcdPGg2IhCQgS6hN7ViRGOHDCPGuLnSDTV_gIkMakXUuruq5uZI2ymmXudXzWqfVZRKsD5VsTAMikgV2SOi-kE) | ![](https://lh7-us.googleusercontent.com/3p9WA5cczYXgJpdoEupRBxspQGWz_2sNVaVXMx39AevRctoEAKr39cxtkH7o2j6kejcdPGg2IhCQgS6hN7ViRGOHDCPGuLnSDTV_gIkMakXUuruq5uZI2ymmXudXzWqfVZRKsD5VsTAMikgV2SOi-kE) |
| <p><br></p> | Шлейф FAN1 2pin             | ![](https://lh7-us.googleusercontent.com/3p9WA5cczYXgJpdoEupRBxspQGWz_2sNVaVXMx39AevRctoEAKr39cxtkH7o2j6kejcdPGg2IhCQgS6hN7ViRGOHDCPGuLnSDTV_gIkMakXUuruq5uZI2ymmXudXzWqfVZRKsD5VsTAMikgV2SOi-kE) | ![](https://lh7-us.googleusercontent.com/3p9WA5cczYXgJpdoEupRBxspQGWz_2sNVaVXMx39AevRctoEAKr39cxtkH7o2j6kejcdPGg2IhCQgS6hN7ViRGOHDCPGuLnSDTV_gIkMakXUuruq5uZI2ymmXudXzWqfVZRKsD5VsTAMikgV2SOi-kE) |
| <p><br></p> | Шлейф T0 2pin               | ![](https://lh7-us.googleusercontent.com/3p9WA5cczYXgJpdoEupRBxspQGWz_2sNVaVXMx39AevRctoEAKr39cxtkH7o2j6kejcdPGg2IhCQgS6hN7ViRGOHDCPGuLnSDTV_gIkMakXUuruq5uZI2ymmXudXzWqfVZRKsD5VsTAMikgV2SOi-kE) | ![](https://lh7-us.googleusercontent.com/3p9WA5cczYXgJpdoEupRBxspQGWz_2sNVaVXMx39AevRctoEAKr39cxtkH7o2j6kejcdPGg2IhCQgS6hN7ViRGOHDCPGuLnSDTV_gIkMakXUuruq5uZI2ymmXudXzWqfVZRKsD5VsTAMikgV2SOi-kE) |
| <p><br></p> | Шлейф E0-MOTOR 4pin         | ![](https://lh7-us.googleusercontent.com/fZ2EifGvIgggK2p9quseoaXvxaxtnF6EDsB9Wrc7x8O5jMmdUWaQU3GZ9WkIQqAkX8C-FBKKOe0aH4fgWufpHTtGuGZkPpZgCssn6RDGEUFQCB-neAMkpEwghFeUDB0bcVegBIwSP8xy3MbRmlnFd5E) | ![](https://lh7-us.googleusercontent.com/fZ2EifGvIgggK2p9quseoaXvxaxtnF6EDsB9Wrc7x8O5jMmdUWaQU3GZ9WkIQqAkX8C-FBKKOe0aH4fgWufpHTtGuGZkPpZgCssn6RDGEUFQCB-neAMkpEwghFeUDB0bcVegBIwSP8xy3MbRmlnFd5E) |

Описание:

Соединяем разъемы платы управления Spider и платы Extension v2.2 в соответствии с таблицей и картинкой

| Наименование разъема платы управления Spider v3 | Наименование разъема платы Extension v2.2 |
| ----------------------------------------------- | ----------------------------------------- |
| HEAT0                                           | HOTEND                                    |
| X-MIN                                           | X-                                        |
| Z-MIN                                           | Z-                                        |
| FAN5                                            | LED-CTRL                                  |
| FAN0                                            | FAN0                                      |
| FAN1                                            | FAN1                                      |
| T0                                              | TE0                                       |
| E0-MOTOR                                        | E0                                        |

\
\




### Подключение одноплатника RockPI

\


| <p><br></p> | Шлейф DuPont 40p – XH2.54-2p                               | 40 см                                                                                                                                                                                             | ![](https://lh7-us.googleusercontent.com/1vT1DjZDkS6EqN0ndsFfW7B3DLVByHDyGUgwfxj5yJFzdU-dX-tSv4BjgSjotOq5kA8ZK10aslLLBciIlanvBe3x2DJHrxv-gpGSTT5aEDV8atYE5TV7hrx03T8lH2_3AMgunYdi9LZ3r9SPLgqRkkI) | ![](https://lh7-us.googleusercontent.com/3p9WA5cczYXgJpdoEupRBxspQGWz_2sNVaVXMx39AevRctoEAKr39cxtkH7o2j6kejcdPGg2IhCQgS6hN7ViRGOHDCPGuLnSDTV_gIkMakXUuruq5uZI2ymmXudXzWqfVZRKsD5VsTAMikgV2SOi-kE) | Шнур USB-A – USB-C | 25 см                                                                                                                                                                                             | ![](https://lh7-us.googleusercontent.com/3jSiAvnLYFNOn6K485nI252hIw_RK-bhCU6KcoEahxpM4rRXx_EOZWHsddAT10V_8QoCteZ5KT715cikpNoqktESjZ7lbduusy7LXPMhqJ8SB1pBaV5FHMxF6w7lVD1hdJpP6YlrEr34K7XVteAK8ho) | <p><br></p> |
| ----------- | ---------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------- |
| <p><br></p> | Шнур ethernet-ethernet на панель (для S400 шнур папа-папа) | ![](https://lh7-us.googleusercontent.com/jhbPEQS4TpgAbiTsqfgPWdG1qjdcXNJLfJPMJ53Zu8sQanqnB16MpL5-D_fbvvZMFcvRfnuuHzSSCzylq90us3q02gfJOLDwOk_1SMhTu1WukAAr9h18LZ8wm-HN39LctU8d9XNPp4etMH8fjIsPCuw) | ![](https://lh7-us.googleusercontent.com/x6oKNUQaPv7Owa76nSnaD7r6KNjNRNykwqMd4Ow8tDNgagCAN08JKVH7KvHtmcwmKydxSiFZe4IwQ5DEceYFvP1_Bfg1xEv-oPW6NJSewxcOESKtZF_UXKnztWGeVYNoyxf9XhpfYu6O6sYK_l_7rFE) | Шнур USB-A – USB-C                                                                                                                                                                                | 50 см              | ![](https://lh7-us.googleusercontent.com/3jSiAvnLYFNOn6K485nI252hIw_RK-bhCU6KcoEahxpM4rRXx_EOZWHsddAT10V_8QoCteZ5KT715cikpNoqktESjZ7lbduusy7LXPMhqJ8SB1pBaV5FHMxF6w7lVD1hdJpP6YlrEr34K7XVteAK8ho) | <p><br></p>                                                                                                                                                                                       |             |
| <p><br></p> | Шнур USB-USB на панель (для S400 шнур папа-папа)           | ![](https://lh7-us.googleusercontent.com/aEXHeNSHdPHQSWFb_HdaM5QXazl5UFl7iZeOP7u1h8Lc6KgRVarBj6j9jY6YWny2DKUgrJi4Vac-0v70jvEtoVP0CbPJqMaOBrmai0K0W0Bo19-t8nAUZk_4YfY_bGDR3wGyaNYjAaaaW32jFNUBJGQ) | ![](https://lh7-us.googleusercontent.com/T78JJfaOr_TAoRm81PhwXVetQ7Xyls1Np4nsjgDa_AkoOGwKlD5FDW-m7KLFjSgg-Iz5Mi8ngLOvCiAbXjLgf7zXyT9AfImHaybvvm6p6xurh_v15TGDu2AbL5eaMDVAzFao60oAXVsmwBsHfasr8SM) | Шлейф FAN\_CH\_CTRL 3pin                                                                                                                                                                          | <p><br></p>        | ![](https://lh7-us.googleusercontent.com/nGbtAiurH_FeWrNQSZpJe42BGepzsk12w4a_IsJvbMCPc8cNYq0AGlIz3bwk6tmHMi5Xy0YbXBkEde0Db8x3hid55zsi-i5RNkOp9ju0JkgzqMgsN6-fL0k_WRZgip1FF5Tzuiw2uQiAuHA_HFE-pv8) | ![](https://lh7-us.googleusercontent.com/nGbtAiurH_FeWrNQSZpJe42BGepzsk12w4a_IsJvbMCPc8cNYq0AGlIz3bwk6tmHMi5Xy0YbXBkEde0Db8x3hid55zsi-i5RNkOp9ju0JkgzqMgsN6-fL0k_WRZgip1FF5Tzuiw2uQiAuHA_HFE-pv8) | <p><br></p> |

\


Подключаем к одноплатнику RockPi 40-пиновый разъем с одним проводом, фиксируем термоклеем!

Устанавливаем одноплатник RockPi на нейлоновые стойки-защелки (прикручиваем к латунным стойкам в случае с S400/S400 HT). Провод с разъемом XH2.54-2p подключаем к разъему ON на плате PSU (смотрим на картинку).

Шнур USB 25см, отмеченный на картинке желтым цветом подключать к плате PSU не нужно, его просто уложить рядом с платой!

Подключаем плату управления Spider USB шнуром к RockPI (на картинке показан черным)

Для S400/S400 HT провода USB и Ethernet от RockPI ведем в правый нижний угол ЭБ (отмечено на картинке оранжевым кружком!)

\


***

\


### Подключаем проводку подсветки в плату расширения

\


Провода для S300 Провода для S400

<table data-header-hidden data-full-width="true"><thead><tr><th></th><th></th><th></th><th></th><th></th><th></th><th></th><th></th><th></th></tr></thead><tbody><tr><td>Черный 0.5 кв.мм</td><td>47см</td><td><img src="https://lh7-us.googleusercontent.com/aH4xMuyHLnIH_cPQrHN7NVI9vrYUMNfERcixtkdyADrW_hMRyjfN5Gs_j0PSRvusaOniLOp4wt5SNIeKiuL3LZgsQzBzom_C4r78gxpwr4qhFXOc9hv-99u89H9S35eQM8_77Y1rnRv6UgLsYI4sKtQ" alt=""></td><td><img src="https://lh7-us.googleusercontent.com/BDrfC_khZDn5-pnaQAjWUTzZntO3QLYdDA1Nwk5Sof0kOSuJpJh_534M3u1Dok70iEcJdVGSKqMG3j3kFnTjZNjIheZm2IKzciM4jTcwbQATtZhJunrQzudUOSkGVkP5TyADPpmaZkfPHdy6lMr_XdQ" alt=""></td><td><br></td><td>Черный 0.5 кв.мм</td><td>47см</td><td><img src="https://lh7-us.googleusercontent.com/aH4xMuyHLnIH_cPQrHN7NVI9vrYUMNfERcixtkdyADrW_hMRyjfN5Gs_j0PSRvusaOniLOp4wt5SNIeKiuL3LZgsQzBzom_C4r78gxpwr4qhFXOc9hv-99u89H9S35eQM8_77Y1rnRv6UgLsYI4sKtQ" alt=""></td><td><img src="https://lh7-us.googleusercontent.com/BDrfC_khZDn5-pnaQAjWUTzZntO3QLYdDA1Nwk5Sof0kOSuJpJh_534M3u1Dok70iEcJdVGSKqMG3j3kFnTjZNjIheZm2IKzciM4jTcwbQATtZhJunrQzudUOSkGVkP5TyADPpmaZkfPHdy6lMr_XdQ" alt=""></td></tr><tr><td>Красный 0.5 кв.мм</td><td>47см</td><td><img src="https://lh7-us.googleusercontent.com/aH4xMuyHLnIH_cPQrHN7NVI9vrYUMNfERcixtkdyADrW_hMRyjfN5Gs_j0PSRvusaOniLOp4wt5SNIeKiuL3LZgsQzBzom_C4r78gxpwr4qhFXOc9hv-99u89H9S35eQM8_77Y1rnRv6UgLsYI4sKtQ" alt=""></td><td><img src="https://lh7-us.googleusercontent.com/BDrfC_khZDn5-pnaQAjWUTzZntO3QLYdDA1Nwk5Sof0kOSuJpJh_534M3u1Dok70iEcJdVGSKqMG3j3kFnTjZNjIheZm2IKzciM4jTcwbQATtZhJunrQzudUOSkGVkP5TyADPpmaZkfPHdy6lMr_XdQ" alt=""></td><td><br></td><td>Красный 0.5 кв.мм</td><td>47см</td><td><img src="https://lh7-us.googleusercontent.com/aH4xMuyHLnIH_cPQrHN7NVI9vrYUMNfERcixtkdyADrW_hMRyjfN5Gs_j0PSRvusaOniLOp4wt5SNIeKiuL3LZgsQzBzom_C4r78gxpwr4qhFXOc9hv-99u89H9S35eQM8_77Y1rnRv6UgLsYI4sKtQ" alt=""></td><td><img src="https://lh7-us.googleusercontent.com/BDrfC_khZDn5-pnaQAjWUTzZntO3QLYdDA1Nwk5Sof0kOSuJpJh_534M3u1Dok70iEcJdVGSKqMG3j3kFnTjZNjIheZm2IKzciM4jTcwbQATtZhJunrQzudUOSkGVkP5TyADPpmaZkfPHdy6lMr_XdQ" alt=""></td></tr><tr><td>Витая пара красный+красный 0.5 кв.мм </td><td>55 см</td><td><img src="https://lh7-us.googleusercontent.com/hJUVJxmpWBjzLv9CI90pNrV6O5JS0PM_oNwduzR5USi0TPuzcjyBvnYOUPq2zctdjq6IMgPqRkbJep8j0j5uBp3H24wA0EqslMsaa_jlRiKTxUqGQNDmPzO4SQSF2_pwCy_9LADjWYAR9MzSA-dbwAI" alt=""></td><td><img src="https://lh7-us.googleusercontent.com/hJUVJxmpWBjzLv9CI90pNrV6O5JS0PM_oNwduzR5USi0TPuzcjyBvnYOUPq2zctdjq6IMgPqRkbJep8j0j5uBp3H24wA0EqslMsaa_jlRiKTxUqGQNDmPzO4SQSF2_pwCy_9LADjWYAR9MzSA-dbwAI" alt=""></td><td><br></td><td>Витая пара красный+красный 0.5 кв.мм </td><td>XX см</td><td><img src="https://lh7-us.googleusercontent.com/hJUVJxmpWBjzLv9CI90pNrV6O5JS0PM_oNwduzR5USi0TPuzcjyBvnYOUPq2zctdjq6IMgPqRkbJep8j0j5uBp3H24wA0EqslMsaa_jlRiKTxUqGQNDmPzO4SQSF2_pwCy_9LADjWYAR9MzSA-dbwAI" alt=""></td><td><img src="https://lh7-us.googleusercontent.com/hJUVJxmpWBjzLv9CI90pNrV6O5JS0PM_oNwduzR5USi0TPuzcjyBvnYOUPq2zctdjq6IMgPqRkbJep8j0j5uBp3H24wA0EqslMsaa_jlRiKTxUqGQNDmPzO4SQSF2_pwCy_9LADjWYAR9MzSA-dbwAI" alt=""></td></tr><tr><td>Черный 0.5 кв.мм</td><td>53 см.</td><td><img src="https://lh7-us.googleusercontent.com/hJUVJxmpWBjzLv9CI90pNrV6O5JS0PM_oNwduzR5USi0TPuzcjyBvnYOUPq2zctdjq6IMgPqRkbJep8j0j5uBp3H24wA0EqslMsaa_jlRiKTxUqGQNDmPzO4SQSF2_pwCy_9LADjWYAR9MzSA-dbwAI" alt=""></td><td><img src="https://lh7-us.googleusercontent.com/hJUVJxmpWBjzLv9CI90pNrV6O5JS0PM_oNwduzR5USi0TPuzcjyBvnYOUPq2zctdjq6IMgPqRkbJep8j0j5uBp3H24wA0EqslMsaa_jlRiKTxUqGQNDmPzO4SQSF2_pwCy_9LADjWYAR9MzSA-dbwAI" alt=""></td><td><br></td><td>Черный 0.5 кв.мм</td><td>XX см</td><td><img src="https://lh7-us.googleusercontent.com/hJUVJxmpWBjzLv9CI90pNrV6O5JS0PM_oNwduzR5USi0TPuzcjyBvnYOUPq2zctdjq6IMgPqRkbJep8j0j5uBp3H24wA0EqslMsaa_jlRiKTxUqGQNDmPzO4SQSF2_pwCy_9LADjWYAR9MzSA-dbwAI" alt=""></td><td><img src="https://lh7-us.googleusercontent.com/hJUVJxmpWBjzLv9CI90pNrV6O5JS0PM_oNwduzR5USi0TPuzcjyBvnYOUPq2zctdjq6IMgPqRkbJep8j0j5uBp3H24wA0EqslMsaa_jlRiKTxUqGQNDmPzO4SQSF2_pwCy_9LADjWYAR9MzSA-dbwAI" alt=""></td></tr></tbody></table>

Описание:

На картинке показан вариант подключения для S300. Для S400 тоже самое, только блок питания другой. Обращайте внимание на наименование клемм блока питания!

### Подключение шлейфов шаговых моторов

Подключаем шлейфы и разводим их, как на картинке ниже, вешаем ферритовые кольца на все 5 шлейфов возле спайдера.

![](file:///C:/Users/Vlad/AppData/Local/Temp/msohtmlclip1/01/clip_image005.png)\


### Установка драйверов ШД

Для S300 устанавливаем 5 драйверов шаговых моторов в Fysetc Spider. Соблюдаем полярность.

Для S400 устанавливаем все 8 драйверов шаговых моторов. Соблюдаем полярность

<figure><img src="https://lh7-us.googleusercontent.com/XecM1ujskug6sBmHlIVJrlI9NISljjJXvI6DmEf1cMY_r80GgXxjV7wNLnwBeVK-C0TMw_FcUQEAgVPN70p95nJjNj3x3zJ_wPWHQWqF-KnTZVMKcIm6dZeF-rLkhLM0hA6Xk8vt291fEJCTr31w7gs" alt=""><figcaption></figcaption></figure>

\
