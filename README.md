# quant_LAA

# Lethargic Asset Allocation

| 비중 | 내용 | ETF | 특징 |
| --- | --- | --- | --- |
| 25% | 고정자산 - 미국 대형주 | IWD | expense ratio 0.19%, dividend 1.57% Russell 1000 Value Index |
| 25% | 고정자산 - 미국 중기 채권 | IEF | expense ratio 0.19%, dividend 0.87% |
| 25% | 고정자산 - 금 | GLD | expense ratio 0.19% |
|  | 변동자산 - 나스닥  | QQQ | expense ratio 0.20%, dividend 0.45% |
|  | 변동자산 - 미국 단기 채권 / 현금 | SHY | expense ratio 0.15%, dividend 0.30% |

매수전략 :
- 자산의 각 25%를 미국 대형가치주, 금, 미국 중기국채에 투자 및 보유
- 자산의 나머지 25%는 QQQ or SHY에 투자  
```
  if (SPY < MA(200) and UNRATE > MA(12))  
    buy SHY  
  else  
    buy QQQ  
```

* 실업률 > 12개월 이동평균 = 불경기
* 실업률 < 12개월 이동평균 = 호경기
* SPY > 200일 이동평균 = 상승장
* SPY < 200일 이동평균 = 하락장

매도전략:
- 연 1회 리밸런싱(고정자산)
- 월 1회 리밸런싱(변동 자산)
    
논문 링크 : <https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3498092> 
