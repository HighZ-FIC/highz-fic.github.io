## About CHARMNET

Our Center is supported by the National Nuclear Security Administration of the U.S. Department of Energy.

----

## Our Team 

{% set members = ['A_Christlieb',  'B_Oshea', 'Q_Tang'] %}

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

