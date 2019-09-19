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

### 5. Code examples (latest React)

<details>
  <summary>FormContainer.js</summary>
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
  <summary>FormComponent.js</summary>
  <pre>
    import React from 'react'

    function FormComponent(props) {
      return (
        <form onSubmit={props.handleSubmit}>
            <input
              type='text'
              value={props.firstName}
              name='firstName'
              placeholder='first name'
              onChange={props.handleChange}
            />
            <br />
            <input
              type='text'
              value={props.lastName}
              name='lastName'
              placeholder='last name'
              onChange={props.handleChange}
            />
            <h1>{props.firstName} {props.lastName}</h1>
            <textarea
              value={props.textArea}
              name='textArea'
              onChange={props.handleChange}
            />
            <br />
            <label>
              <input
                type='checkbox'
                name='isFriendly'
                checked={props.isFriendly}
                onChange={props.handleChange}
              /> you are friendly?
            </label>
            <br />
            <label>
              <input
                type='radio'
                name='gender'
                value='male'
                checked={props.gender === 'male'}
                onChange={props.handleChange}
              /> male
            </label>
            <br />
            <label>
              <input
                type='radio'
                name='gender'
                value='female'
                checked={props.gender === 'female'}
                onChange={props.handleChange}
              /> female
            </label>
            <br />
            <label>your favorite color? </label>
            <select
              value={props.favColor}
              onChange={props.handleChange}
              name='favColor'
            >
              <option value='red'>red</option>
              <option value='green'>green</option>
              <option value='blue'>blue</option>
            </select>
            <h2>you choose:  {'' + props.isFriendly} {props.gender} {props.favColor}</h2>
            <button>submit</button>
          </form>
      )
    }

    export default FormComponent
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
