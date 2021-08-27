# Token Economics

The native Fungible Token for Shroom Kingdom is called Shroom and has the symbol SHRM.
Fungible Tokens do not differ from each other and are a common way to develop "money-like" tokens.

Since SHRM is commonly minted by playing on Shroom Kingdom, there is no upper limit.
Instead, a constant minting and burning mechanism should make sure, that the token's value
won't suffer from inflation or deflation.

Also keep in mind, that this document often talks about minting, but in fact the tokens
do not yet exist on-chain.
Instead they will be stored in an off-chain database first.
The user can then decide to mint its SHRM tokens by calling a Smart Contract.
This mechanism is explained more in depth in the [Smart Contract details](#smart-contract-details)

## Minting and burning

SHRM tokens will be minted by one of the following tasks:

- finishing a level (max 5 x 1 SHRM / day)
- voting/rating a level (max 1 x 3 SHRM / day)
- daily challenges (5 SHRM / day)
- passive generation while others play own levels (max 8 SHRM / day).

SHRM tokens will be burned by one of the following tasks:

- unlocking new building blocks and entities that can be placed in levels (token amount varies)
- minting of levels (100 SHRM)
- challenge passes (tbd)
- virtual land acquisition and NFTs involved (tbd)

Since Shroom Kingdom will launch with relatively few game mechanics as a Minimum Viable Product,
there won't be many ways for burning SHRM tokens.
Once more game mechanics will be implemented, there will also be more ways to burn tokens.
To prevent inflation in the early days after launch, a multiplier will be applied to all previously
mentioned minting mechanisms.

To make sure that every kind of player enjoys playing on Shroom Kingdom, the SHRM token minting
will be capped at 13 SHRM per day (8 SHRM for playing/building + 5 SHRM for daily).
Players can either decide whether they want to earn their tokens by playing or building levels
or by a combination of both.

## Initial SHRM token launch & funding

Shroom Kingdom will be community funded.
No Venture Capital is involved.
An initial <a href="//www.sputnik.fund/#/dao/humanguild.sputnikdao.near/proposals/25" target="_blank" rel="noreferrer noopener">
funding round{{#include icons/link.svg}}</a> also happened with
<a href="//humanguild.io/" target="_blank" rel="noreferrer noopener">Human Guild{{#include icons/link.svg}}</a>.

For the initial distribution of the token, 10 million SHRM tokens will be minted on launch.
These tokens will be distributed as the following:

<script type="text/javascript" src="//cdn.amcharts.com/lib/4/core.js"></script>
<script type="text/javascript" src="//cdn.amcharts.com/lib/4/charts.js"></script>
<script type="text/javascript" src="//cdn.amcharts.com/lib/4/themes/dark.js"></script>
<script type="text/javascript">
  am4core.useTheme(am4themes_dark);
  var chart = am4core.createFromConfig({
    series: [{
      type: "PieSeries3D",
      dataFields: {
        value: "share",
        category: "category"
      },
      slices: {
        stroke: "#fff",
        strokeWidth: 2,
        strokeOpacity: 1,
        fillOpacity: 1,
        states: {
          hover: {
            properties: {
              scale: 1,
              fillOpacity: 0.5
            }
          }
        },
        propertyFields: {
          fill: "color"
        }
      }
    }],
    innerRadius: am4core.percent(40),
    data: [
      {
        category: "founder",
        share: "1500000",
        color: "#495fba"
      },
      {
        category: "DAO",
        share: "4500000",
        color: "#e8d685"
      },
      {
        category: "IDO",
        share: "3000000",
        color: "#ae85c9"
      },
      {
        category: "Liquidity",
        share: "750000",
        color: "#c9f0e1"
      },
      {
        category: "Airdrops",
        share: "250000",
        color: "#d48652"
      }
    ],
    legend: {
      valueLabels: {
        text: "{value.value}"
      }
    },
    numberFormatter: {
      numberFormat: "#.0a"
    },
  }, "token-distribution-chart", am4charts.PieChart3D);
</script>
<div id="token-distribution-chart" style="width: 100%; height: 400px; background-color: #282828;" ></div>

## Initial DEX Offering (IDO)

An Initial DEX Offering is planned to launch on <a href="//skyward.finance/" target="_blank" rel="noreferrer noopener">
Skyward Finance{{#include icons/link.svg}}</a>.
The revenue of the IDO will be distributed as the following:

<script type="text/javascript">
  am4core.useTheme(am4themes_dark);
  var chart = am4core.createFromConfig({
    series: [{
      type: "PieSeries3D",
      dataFields: {
        value: "share",
        category: "category"
      },
      labels: {
        text: "{category}: {value.percent}%"
      },
      slices: {
        stroke: "#fff",
        strokeWidth: 2,
        strokeOpacity: 1,
        fillOpacity: 1,
        states: {
          hover: {
            properties: {
              scale: 1,
              fillOpacity: 0.5
            }
          }
        },
        propertyFields: {
          fill: "color"
        },
        tooltipText: "{category}: {value.percent}%"
      }
    }],
    innerRadius: am4core.percent(40),
    data: [
      {
        category: "founder",
        share: "20%",
        color: "#495fba"
      },
      {
        category: "DAO",
        share: "55%",
        color: "#e8d685"
      },
      {
        category: "Liquidity",
        share: "25%",
        color: "#c9f0e1"
      }
    ],
    legend: {
      valueLabels: {
        text: "{value.percent}%"
      }
    },
    numberFormatter: {
      numberFormat: "#."
    },
  }, "ido-chart", am4charts.PieChart3D);
</script>
<div id="ido-chart" style="width: 100%; height: 400px; background-color: #282828;" ></div>

The IDO will be launched in three phases with increasing token amount,
because more people will become interested over time about Shroom Kingdom.
The exact token amounts are:

- 750,000 SHRM (date will be announced)
- 1,000,000 SHRM (two months later)
- 1,250,000 SHRM (two months later)

## Smart Contract details

The SHRM token Smart Contract needs to be able to mint tokens on demand.
Since tokens are tracked in an off-chain database before minting,
the backend would need to read this information.
Only the backend is allowed to directly read and write values to the database.

To be able to mint new SHRM tokens, the backend would have to read the pending
SHRM token rewards from the off-chain database.
Then it would call the Smart Contract to mint tokens and update the value in the database respectively.
This approach has the drawback, that it could potentially be exploited,
since the backend API would have to pay the gas fees for minting SHRM tokens.

To avoid this problem, a different approach is used where the pending SHRM token rewards will be tracked
in the Smart Contract itself, which will be updated once per day.
The user has then the ability to mint tokens himself by calling the Smart Contract.
As a result the user would have to pay the gas fee for minting and the backend would
only have to pay the gas fee once per day for updating the pending rewards in the Smart Contract.
The only disadvantage of this approach is that pending rewards will be locked for at most 24 hours.
