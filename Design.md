# Design — ENISHI Gift Forge

## Before

「紹介者を連れてきた人にプレゼント」という一文だけでは、紹介成立、対象外、重複、同意、費用、在庫、期限、キャンセル、問い合わせ、公開責任が決まらない。

## After

```text
INTAKE
  -> SOURCE_BOUNDARY
  -> OFFER_DRAFT
  -> REFERRAL_RULES
  -> CONSENT_AND_PRIVACY
  -> FULFILLMENT_DRY_RUN
  -> FOUR_LANE_REVIEW
  -> NEEDS_APPROVAL
  -> APPROVED
  -> FULFILLED
  -> READ_BACK_AND_RECONCILE
```

## Value added

1. 紹介先が自分で登録する同意優先導線
2. 紹介者ID・イベントID・紹介先同意・参加状態を組み合わせた判定
3. 重複・自己紹介・上限・期限・再送・代替を含む履行設計
4. Offer / Experience / Operations / Riskの4レーンレビュー
5. 外部送信・購入・発送・公開を承認payloadとread-backに分離
6. 参照元が読めない場合も、独立設計として出典境界を壊さない
