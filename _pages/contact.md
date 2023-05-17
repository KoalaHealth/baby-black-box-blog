---
title: "Contact"
permalink: "/contact"
---
{% if site.smartforms_endpoint %}
<form action="{{ site.smartforms_endpoint }}" method="POST">    
    <p class="mb-4">Whether you are a parent or partner, we want to hear from you!  Send us your requests, questions, suggestions, and feedback!</p>
    <div class="form-group row">
        <div class="col-md-6">
        <input class="form-control" type="text" name="name" placeholder="Name*" required>
        </div>
        <div class="col-md-6">
        <input class="form-control" type="email" name="email" placeholder="E-mail Address*" required>
        </div>
    </div>
    <textarea rows="8" class="form-control mb-3" name="tel" placeholder="Message*" required></textarea>    
    <input class="btn btn-success" type="submit" value="Send">
</form>
{% elsif site.formspree_endpoint %}

<form action="{{ site.formspree_endpoint }}" method="POST">    
    <p class="mb-4">Whether you are a parent or partner, we want to hear from you!  Send us your requests, questions, suggestions, and feedback!</p>
    <div class="form-group row">
        <div class="col-md-6">
        <input class="form-control" type="text" name="name" placeholder="Name*" required>
        </div>
        <div class="col-md-6">
        <input class="form-control" type="email" name="_replyto" placeholder="E-mail Address*" required>
        </div>
    </div>
    <textarea rows="8" class="form-control mb-3" name="message" placeholder="Message*" required></textarea>    
    <input class="btn btn-success" type="submit" value="Send">
</form>

{% endif %}