# CCS2024b-benchmark
<a href="https://openai.com/product/dall-e-2"><img src="resources/logo.png" alt="Logo" align="right" width="82"/></a>

This project is dedicated to the smart contract dataset of CCS2024b. The repository contains two datasets, including a labelled dataset with 110 annotated cases, and a real-world dataset derived from Code4rena contest.


## Dataset Description

### Small Dataset:
- Contains 110 contract test cases divided into 11 subdatasets.
- Includes 10 subdatasets with known vulnerabilities in the Top 10 categories.
- Provides one subdataset with correct test cases.

### Real-world Dataset:
- Hosts 100 test cases derived from Code4rena contest \url{https://github.com/ZhangZhuoSJTU/Web3Bugs}.

## Folder Description
The dataset is organized into three folders:
+ [labeled/](labeled/): contains our ICSE23 paper summarizing our preliminary results, as well as the supplementary material for the paper.
+ [realworld/](realworld/): contains the bug classification in [bugs.csv](results/bugs.csv) and the description for each contest in [contests.csv](results/contests.csv).
+ [reports/](reports/): contains all the reports provided by code4rena.


## Top 10 categories:
1. Reentrancy
2. Arithmetic
3. Gasless send
4. unsafe suicidal
5. unsafe delegatecall
6. unchecked send
7. TOD
8. time manipulation
9. tx.origin
10. bad randomness


## Labelled dataset:
<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Type</th>
      <th>Description</th>
      <th>Number</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Reentrancy</td>
      <td>This vulnerability occurs when a contract calls an external contract, and the called contract then calls back into the calling contract before the first invocation is finished. </td>
      <td>10</td>   
    </tr>
    <tr>
      <th>1</th>
      <td>Arithmetic</td>
      <td>This occurs when an arithmetic opera- tion generates a value that exceeds the range that can be represented within the fixed number of bits designated for integers in the EVM. </td>
      <td>10</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Unchecked send</td>
      <td>This vulnerability happens when the call fails accidentally or an attacker forces the call to fail. It is also described as ``unhandled exceptions``, ``exception disorder``, or ``unchecked low-level call``.</td>
      <td>10</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Unsafe delegatecall</td>
      <td>This vulnerability rises from the DELEGATECALL instruction, which allows a contract to dynamically load code from another contract at runtime.</td>
      <td>10</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Transaction Ordering Dependence</td>
      <td>This vulnerability, is also described as TOD, arises when a contract’s behaviour depends on the order of transactions.</td>
      <td>10</td>
    </tr>
      <tr>
      <th>5</th>
      <td>Time manipulation</td>
      <td>This vulnerability arises when smart contracts rely on the timestamp information from blocks.</td>
      <td>10</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Bad randomness</td>
      <td>This vulnerability pertains to the flawed generation of random numbers within smart contracts. Random numbers often influence the decisions or outcomes of contract functionalities. </td>
      <td>10</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Authorization through tx.origin</td>
      <td>This vulnerability arises when the tx.origin variable is exploited by attackers. </td>
      <td>10</td>
    </tr>
      <tr>
      <th>8</th>
      <td>Unsafe suicidal</td>
      <td>This vulnerability manifests when the SELFDESTRUCT function is improperly secured and subsequently exploited by attackers. </td>
      <td>10</td>
    </tr>
        <tr>
      <th>9</th>
      <td>Gasless send</td>
      <td>This vulnerability occurs when there’s an insufficient amount of gas to carry out an external call, resulting in the reversion of the transaction.</td>
      <td>10</td>
    </tr>
        <tr>
      <th>10</th>
      <td>Safe contracts</td>
      <td>This subdataset contains no vulnerable contracts</td>
      <td>10</td>
    </tr>
  </tbody>
</table>
</div>
