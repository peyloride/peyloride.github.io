---
title: İletişim
permalink: "/contact/"
layout: page
---

<form id="contact-form" class="form" action="https://getsimpleform.com/messages?form_api_token=ba690eab9a23b8c1a4b6e186bccf644f" method="POST" enctype="multipart/form-data">
        <ul class="contact-ul">
            <li class="contact-li">
                <label class="contact-label" for="name">İsim:</label>
                <input type="text" placeholder="Adınız soyadınız" id="name" class="contact-input" name="name" tabindex="1"/>
            </li>
            <li class="contact-li">
                <label class="contact-label" for="email">Email:</label>
                <input type="email" placeholder="Geri dönüş için email adresiniz" id="email" class="contact-input" name="email" tabindex="2"/>
            </li>
            <li class="contact-li">
                <label class="contact-label" for="message">Mesajınız:</label>
                <textarea class="contact-textarea" placeholder="Herhangi bir konuda iletişime geçebilirsiniz." rows="5" id="message" name="message" tabindex="3"></textarea>
            </li>

        </ul>
        <input type="submit" value="Gönder" id="submit"/>
        <input type="hidden" name='redirect_to' value="{{site.url}}/thank-you/" />

</form>




<style>

.contact-li {
    list-style: none;
}

.contact-input {
    border:none;
    border-bottom: 1px solid #eee;
    transition-duration: 0.3s;
    width: 100%;
}

.contact-input:focus {
    outline:none;
    border-bottom: 1px solid #e74c3c;
}

.contact-textarea {
    border:none;
    border-bottom: 1px solid #eee;
    transition-duration: 0.3s;
    width: 100%;
}

.contact-textarea:focus {
    outline:none;
    border-bottom: 1px solid #e74c3c;
}

.contact-label {
    display: block;
}

ul.contact-ul {
    margin: 0;
    padding: 10px;
    width: 100%;
}

#submit {
    border:none;
    background-color: #e74c3c;
    padding: 5px 15px;
    color: #eee;
    opacity: 0.8;
}

#submit:hover {
    opacity: 1;
    cursor: pointer;
}


#contact-form {
    border: 1px solid #aaa;
    display: inline-flex;
    margin-bottom: 1em;
    width: 100%;
}

</style>
