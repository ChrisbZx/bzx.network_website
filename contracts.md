---
layout: page-wide-container
permalink: contracts
metadescription: "bZx Protocol v2 Smart Contracts List"
featured-image: /images/ogp.png
title: bZx Smart Contracts List
h1title: bZx Protocol v2 Smart Contracts List
---
<div class="container container-xl">
    <h3 class="fs-24 fs-sm-20 fw-700 lh-160 lh-xs-150 mb-15 color-primary text-center mb-30">Smart Contracts</h3>
    <div class="buttons-tabs-itokens">
        <button class="tablinks-itokens active" data-itokens="itokens-mainnet">Mainnet</button>
        <button class="tablinks-itokens" data-itokens="itokens-kovan">Kovan</button>
    </div>
    <div id="itokens-mainnet" class="tabcontent-itokens active">
        <table class="table-itokens">
            <thead>
                <tr>
                    <td class="thead-ticker">Ticker</td>
                    <td class="thead-address">Address</td>
                    <td class="thead-description">Description</td>
                    <td class="thead-icon">Icon</td>
                </tr>
            </thead>
            <tbody>
                {% for mainnet in site.data.itokens[0].mainnet %}
                    <tr>
                        <td class="ticker">{{mainnet.ticker}}</td>
                        <td class="address"><a href="https://etherscan.io/address/{{ mainnet.address }}" target="_blank">{{mainnet.address}}</a></td>
                        <td class="description">{{mainnet.description}}</td>
                        <td class="icon"><div class="itoken-gradient"><div class="itoken-white">{% include svg/itokens/{{mainnet.ticker}}.svg %}</div></div></td>
                    </tr>
                {% endfor %}
                {% for mainnet in site.data.itokens[0].mainnetprotocoldetails %}
                    <tr>
                        <td class="ticker">{{mainnet.ticker}}</td>
                        <td class="address"><a href="https://etherscan.io/address/{{ mainnet.address }}" target="_blank">{{mainnet.address}}</a></td>
                        <td class="description">{{mainnet.description}}</td>
                        <td class="icon"><div class="itoken-gradient"><div class="itoken-white"><div class="svg-gradient">{% include svg/BZRX.svg %}</div></div></div></td>
                    </tr>
                {% endfor %}
            </tbody>
        </table>
    </div>
    <div id="itokens-kovan" class="tabcontent-itokens">
        <table class="table-itokens">
            <thead>
                <tr>
                    <td class="thead-ticker">Ticker</td>
                    <td class="thead-address">Address</td>
                    <td class="thead-description">Description</td>
                    <td class="thead-icon">Icon</td>
                </tr>
            </thead>
            <tbody>
                {% for kovan in site.data.itokens[1].kovan %}
                    <tr>
                        <td class="ticker">{{kovan.ticker}}</td>
                        <td class="address"><a href="https://kovan.etherscan.io/address/{{ kovan.address }}" target="_blank">{{kovan.address}}</a></td>
                        <td class="description">{{kovan.description}}</td>
                        <td class="icon"><div class="itoken-gradient"><div class="itoken-white">{% include svg/itokens/{{kovan.ticker}}.svg %}</div></div></td>
                    </tr>
                {% endfor %}
                {% for kovan in site.data.itokens[1].kovanprotocoldetails %}
                    <tr>
                        <td class="ticker">{{kovan.ticker}}</td>
                        <td class="address"><a href="https://kovan.etherscan.io/address/{{ kovan.address }}" target="_blank">{{kovan.address}}</a></td>
                        <td class="description">{{kovan.description}}</td>
                        <td class="icon"><div class="itoken-gradient"><div class="itoken-white"><div class="svg-gradient">{% include svg/BZRX.svg %}</div></div></div></td>
                    </tr>
                {% endfor %}
            </tbody>
        </table>
    </div>
</div>
