# Frontend Developer

### 1. Name

Evgeny Ivanov

---

### 2. Contact Info

Email: [ineg22@gmail.com](mailto:ineg22@gmail.com)
Phone: [+375 (29) 757-36-51](tel:+375297573651)
Telegram: [@ineg_xd](https://t.me/ineg_xd)

---

### 3. Summary

In an attempt to change the field of activity, I have been self-taught for six months. 
It is important for me to get the maximum amount of new knowledge from this course.

---

### 4. Skills

- HTML
- CSS
- git
- JS
- React

---

### 5. Code examples

<details>
  <summary>FormContainer.js (react task)</summary>
  <pre>
    import React from 'react'
    import FormComponent from './FormComponent'

    class FormContainer extends React.Component {
      constructor() {
        super();
        this.state = {
          firstName: 'vasya',
          lastName: 'pupkin',
          isFriendly: true, 
          textArea: 'some default value',
          gender: 'female',
          favColor: 'blue',
        };
        this.handleChange = this.handleChange.bind(this)
        this.handleSubmit = this.handleSubmit.bind(this)
      }

      handleChange(evt) {
        const { name, value, type, checked } = evt.target
        type === 'checkbox' ? this.setState({ [name]: checked }) : this.setState({ [name]: value })
      }

      handleSubmit(evt) {
        console.log(this.state);
        evt.preventDefault();
      }

      render() {
        return (
          <FormComponent 
            handleChange={this.handleChange}
            handleSubmit={this.handleSubmit}
            {...this.state} // data={this.state} => in component props.data instead props
            />
        );
      }
    }

    export default FormContainer
  </pre>
</details>
<details>
  <summary>gallery.js (HTML academy task)</summary>
  <pre>
    'use strict';
    (function () {

      var pictureTemplate = document.querySelector('#picture').content.querySelector('.picture__link');
      var picturesContainer = document.querySelector('.pictures');
      var fragment = document.createDocumentFragment();

      var pictures = [];
      for (var i = 0; i < 25; i++) {
        pictures.push(generatePicture());
      }

      for (i = 0; i < pictures.length; i++) {
        fragment.appendChild(renderPicture(pictures[i]));
      }
      picturesContainer.appendChild(fragment);

      function generatePicture() {
        var obj = {};
        var photoId = pictures.length + 1;
        obj.id = photoId;
        obj.url = 'photos/' + photoId + '.jpg';
        obj.likes = window.utils.randomSelect(15, 200);
        obj.description = window.data.DESCRIPTIONS_ARRAY[window.utils.randomSelect(0, window.data.DESCRIPTIONS_ARRAY.length - 1)];
        obj.comments = [];
        var commentsCount = window.utils.randomSelect(1, 3);
        for (var i = 0; i < commentsCount; i++) {
          obj.comments.push(window.data.COMMENTS_ARRAY[window.utils.randomSelect(0, window.data.COMMENTS_ARRAY.length - 1)]);
        }
        return obj;
      }

      function renderPicture(obj) {
        var pictureElement = pictureTemplate.cloneNode(true);
        pictureElement.querySelector('.picture__img').setAttribute('src', obj.url);
        pictureElement.querySelector('.picture__stat--likes').textContent = '' + obj.likes;
        pictureElement.querySelector('.picture__stat--comments').textContent = '' + obj.comments.length;
        pictureElement.querySelector('img').setAttribute('id', obj.id);
        return pictureElement;
      }

      window.gallery = {
        pictures: pictures
      };

      document.querySelector('.img-filters').classList.remove('img-filters--inactive');

    })();

  </pre>
</details>

---

### 6. Experience

- all free HTML and CSS courses on [HTML academy](https://htmlacademy.ru/profile/id987073)
- 80% of [learn.javascript.ru](https://learn.javascript.ru/)
- ~5 free JS webinars
- few free REACT courses on scrimba and freeCodeCamp

---

### 7. Education

> 2009 - 2014 - Belarusian State University (Faculty of Radiophysics and Computer Technologies) 

> 2014 - 2015 - China Academy of Space Technologies (1 year in Beijing)

---

### 8. English

Pre-Intermediate (A2)
