## About HighZ

The HighZ center is a Focused Investigatory Center (FIC) supported by the Predictive Science Academic Alliance Program (PSAAP), managed by the NNSA Office of Advanced Simulation and Computing (ASC).

----

## Our Team 

{% set members = ['A_Christlieb',  'B_Oshea',  'C_Shu',  'Q_Tang'] %}

{% for member in members %}

<div class="row">
    <div class="col-md-2">
        <img src="../bios/{{ member }}.jpg" alt="Missing picture" width="100%">
    </div>
    <div class="col-md-10">
        <br><p>
        {% set bio = "/bios/" + member + ".html" %}
            {% include bio %}
        </p>
    </div>
</div>
{% endfor %}

## PostDoc
 
 Coming Soon

 
## Graduate Students

{% set ssmembers = ['T_Behling', 'T_Burnett',  'H_Harish',  'C_Tseng',  'C_Wendeln' ] %}

{% for member in ssmembers %}

<div class="row">
    <div class="col-md-2">
        <img src="../bios/{{ member }}.jpg" alt="Missing picture" width="100%" height="100%" object-fit=cover>
    </div>
    <div class="col-md-10">
        <br><p>
        {% set bio = "/bios/" + member + ".html" %}
            {% include bio %}
        </p>
    </div>
</div>
{% endfor %}

