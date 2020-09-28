# List Transaction Code

<table>
  <thead>
    <tr>
      <th style="text-align:left">Code</th>
      <th style="text-align:left">Response</th>
      <th style="text-align:left">Detail</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">00</td>
      <td style="text-align:left">Transaction Approved</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">01</td>
      <td style="text-align:left">Refer to card issuer</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">02</td>
      <td style="text-align:left">Refer to card issuer, special condition</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">03</td>
      <td style="text-align:left">Invalid merchant or service provider</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">04</td>
      <td style="text-align:left">Pick up card (no fraud)</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">05</td>
      <td style="text-align:left">Do not honor</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">06</td>
      <td style="text-align:left">General error</td>
      <td style="text-align:left">
        <p>The customer&#x2019;s card issuer has declined the transaction as there
          is a problem with the card number. The customer should contact their card
          issuer and/or use an alternate card.</p>
        <p></p>
        <p>Note: This response code can also be returned via the Rapid API if you
          run a transaction query prior to the transaction being completed.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">07</td>
      <td style="text-align:left">Pick up card, special condition (fraud account)</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">08</td>
      <td style="text-align:left">Honour with Identification</td>
      <td style="text-align:left">Transaction processed successfully - identification NOT required. This
        code is returned by some banks in place of 00 response.</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

#### Reff

* [https://developer.visa.com/guides/request\_response\_codes](https://developer.visa.com/guides/request_response_codes)
* [https://go.eway.io/s/article/Bank-Response-Codes-Responses-00-to-38](https://go.eway.io/s/article/Bank-Response-Codes-Responses-00-to-38)
* [https://go.eway.io/s/article/Bank-Response-Codes-39-to-96](https://go.eway.io/s/article/Bank-Response-Codes-39-to-96)
* [https://developers.google.com/standard-payments/v1/fops/card/response-codes](https://developers.google.com/standard-payments/v1/fops/card/response-codes)

