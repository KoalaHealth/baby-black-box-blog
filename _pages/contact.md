---
title: "Contact"
permalink: "/contact"
---

<div class="row align-items-center">
    <h4 class="mb-4 ml-3 mr-3"><small>Whether you are a parent or partner, we want to hear from you!  We want to read your questions/requests, suggestions/feedback, or even your own real parent stories!</small></h4>
    <div class="col-lg-6">
        <img src="{{ site.baseurl }}/assets/images/welcome-contact.jpg" />
    </div>

    <div  class="col-lg-6">
        {% if site.smartforms_endpoint %}
        <form action="{{ site.smartforms_endpoint }}" method="POST">    
            <div class="form-group row">
                <div class="col-md-6">
                <input class="form-control" type="text" name="name" placeholder="Name*" required>
                </div>
                <div class="col-md-6">
                <input class="form-control" type="email" name="email" placeholder="E-mail Address*" required>
                </div>
            </div>
            <textarea rows="8" class="form-control mb-3" name="tel" placeholder="Message*" required></textarea>    
            <input class="btn btn-success btn-block" type="submit" value="Send">
        </form>
        {% elsif site.formspree_endpoint %}
        <form action="{{ site.formspree_endpoint }}" method="POST">    
            <div class="form-group row">
                <div class="col-md-6">
                <input class="form-control" type="text" name="name" placeholder="Name*" required>
                </div>
                <div class="col-md-6">
                <input class="form-control" type="email" name="_replyto" placeholder="E-mail Address*" required>
                </div>
            </div>
            <textarea rows="8" class="form-control mb-3" name="message" placeholder="Message*" required></textarea>    
            <input class="btn btn-success btn-block" type="submit" value="Send">
        </form>
        {% endif %}
    </div>
</div>