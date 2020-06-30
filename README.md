# Items to be refactored

**Comments in the top of the files that look like this:**
```
/*!

=========================================================
* Paper Dashboard PRO React - v1.2.0
=========================================================

* Product Page: https://www.creative-tim.com/product/paper-dashboard-pro-react
* Copyright 2020 Creative Tim (https://www.creative-tim.com)

* Coded by Creative Tim

=========================================================

* The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

*/
```

Reason: taking extra space with no real reason to be there, plus we don't want that 👆🏾in production code.

| Error Location                               | Has the Error been fixed? |
| -------------------------------------------- | ------------------------- |
| src/index.js                                 | 🙅🏾‍♂️                         |
| src/routes.js                                | 🙅🏾‍♂️                         |
| src/layouts/Admin.js                         | 🙅🏾‍♂️                         |
| src/layouts/Auth.js                          | 🙅🏾‍♂️                         |
| src/variables/icons.js                       | 🙅🏾‍♂️                         |
| src/variables/charts.js                      | 🙅🏾‍♂️                         |
| src/variables/general.js                     | 🙅🏾‍♂️                         |
| src/views/Charts.js                          | 🙅🏾‍♂️                         |
| src/views/Widgets.js                         | 🙅🏾‍♂️                         |
| src/views/Dashboard.js                       | 🙅🏾‍♂️                         |
| src/components/Sidebar/Sidebar.js            | 🙅🏾‍♂️                         |
| src/components/Footer/Footer.js              | 🙅🏾‍♂️                         |
| src/components/FixedPlugin/FixedPlugin.js    | 🙅🏾‍♂️                         |
| src/components/Navbars/AdminNavbar.js        | 🙅🏾‍♂️                         |
| src/components/CustomUpload/ImageUpload.js   | 🙅🏾‍♂️                         |
| src/components/Navbars/AuthNavbar.js         | 🙅🏾‍♂️                         |
| src/components/CustomUpload/PictureUpload.js | 🙅🏾‍♂️                         |
| src/views/maps/VectorMap.js                  | 🙅🏾‍♂️                         |
| src/views/maps/FullScreenMap.js              | 🙅🏾‍♂️                         |
| src/views/maps/GoogleMaps.js                 | 🙅🏾‍♂️                         |
| src/views/Calendar.js                        | 🙅🏾‍♂️                         |
| src/views/tables/ReactTables.js              | 🙅🏾‍♂️                         |
| src/views/tables/ExtendedTables.js           | 🙅🏾‍♂️                         |
| src/views/tables/RegularTables.js            | 🙅🏾‍♂️                         |
| src/views/forms/ExtendedForms.js             | 🙅🏾‍♂️                         |
| src/views/forms/ValidationForms.js           | 🙅🏾‍♂️                         |
| src/views/forms/Wizard.js                    | 🙅🏾‍♂️                         |
| src/views/forms/RegularForms.js              | 🙅🏾‍♂️                         |
| src/views/components/Typography.js           | 🙅🏾‍♂️                         |
| src/assets/scss/paper-dashboard.scss         | 🙅🏾‍♂️                         |
| src/views/components/GridSystem.js           | 🙅🏾‍♂️                         |
| src/views/components/Icons.js                | 🙅🏾‍♂️                         |
| src/views/components/Panels.js               | 🙅🏾‍♂️                         |
| src/views/components/SweetAlert.js           | 🙅🏾‍♂️                         |
| src/assets/css/paper-dashboard.css           | 🙅🏾‍♂️                         |
| src/views/components/Notifications.js        | 🙅🏾‍♂️                         |
| src/views/components/Buttons.js              | 🙅🏾‍♂️                         |
| src/views/pages/Login.js                     | 🙅🏾‍♂️                         |
| src/views/pages/Register.js                  | 🙅🏾‍♂️                         |
| src/views/pages/LockScreen.js                | 🙅🏾‍♂️                         |
| src/views/pages/Timeline.js                  | 🙅🏾‍♂️                         |
| src/views/pages/UserProfile.js               | 🙅🏾‍♂️                         |
| src/views/forms/WizardSteps/Step2.js         | 🙅🏾‍♂️                         |
| src/assets/css/paper-dashboard.min.css       | 🙅🏾‍♂️                         |
| src/views/forms/WizardSteps/Step3.js         | 🙅🏾‍♂️                         |
| src/views/forms/WizardSteps/Step1.js         | 🙅🏾‍♂️                         |

****

**Prefer destructured import of React Component**

Instead of typing `React.Component`, you can use the import statement to destructure the Component off and then if you use the `Component` in the class based Component. Less code, less errors.

_Do this ✅_:
```js
import React, {Component} from 'react'

export default class Home extends Component {
  render() {
    return (
      <div>
        <h1>Home</h1>
      </div>
    )
  }
}
```

_**NOT** this 💩_:
```js
import React from "react";

class Dashboard extends React.Component {
  render() {
    return (
      <div>
        <h1>Dashboard</h1>
      </div>
    )
}

export default Dashboard;
```
| Error Location                               | Has the Error been fixed? |
| -------------------------------------------- | ------------------------- |
| src/layouts/Auth.js                          | 🙅🏾‍♂️                         |
| src/layouts/Admin.js                         | 🙅🏾‍♂️                         |
| src/views/Charts.js                          | 🙅🏾‍♂️                         |
| src/views/Dashboard.js                       | 🙅🏾‍♂️                         |
| src/views/Widgets.js                         | 🙅🏾‍♂️                         |
| src/views/Calendar.js                        | 🙅🏾‍♂️                         |
| src/components/Sidebar/Sidebar.js            | 🙅🏾‍♂️                         |
| src/components/CustomUpload/ImageUpload.js   | 🙅🏾‍♂️                         |
| src/components/CustomUpload/PictureUpload.js | 🙅🏾‍♂️                         |
| src/views/maps/FullScreenMap.js              | 🙅🏾‍♂️                         |
| src/views/maps/GoogleMaps.js                 | 🙅🏾‍♂️                         |
| src/views/tables/RegularTables.js            | 🙅🏾‍♂️                         |
| src/components/Navbars/AuthNavbar.js         | 🙅🏾‍♂️                         |
| src/components/Footer/Footer.js              | 🙅🏾‍♂️                         |
| src/components/Navbars/AdminNavbar.js        | 🙅🏾‍♂️                         |
| src/views/maps/VectorMap.js                  | 🙅🏾‍♂️                         |
| src/views/tables/ReactTables.js              | 🙅🏾‍♂️                         |
| src/views/components/Icons.js                | 🙅🏾‍♂️                         |
| src/views/forms/ExtendedForms.js             | 🙅🏾‍♂️                         |
| src/views/forms/Wizard.js                    | 🙅🏾‍♂️                         |
| src/views/forms/ValidationForms.js           | 🙅🏾‍♂️                         |
| src/views/forms/RegularForms.js              | 🙅🏾‍♂️                         |
| src/views/pages/UserProfile.js               | 🙅🏾‍♂️                         |
| src/views/components/Typography.js           | 🙅🏾‍♂️                         |
| src/views/pages/Register.js                  | 🙅🏾‍♂️                         |
| src/views/pages/Timeline.js                  | 🙅🏾‍♂️                         |
| src/views/components/SweetAlert.js           | 🙅🏾‍♂️                         |
| src/views/components/Notifications.js        | 🙅🏾‍♂️                         |
| src/views/components/Buttons.js              | 🙅🏾‍♂️                         |
| src/views/tables/ExtendedTables.js           | 🙅🏾‍♂️                         |
| src/views/components/GridSystem.js           | 🙅🏾‍♂️                         |
| src/views/components/Panels.js               | 🙅🏾‍♂️                         |
| src/views/pages/Login.js                     | 🙅🏾‍♂️                         |
| src/views/pages/LockScreen.js                | 🙅🏾‍♂️                         |
| src/views/forms/WizardSteps/Step2.js         | 🙅🏾‍♂️                         |
| src/views/forms/WizardSteps/Step3.js         | 🙅🏾‍♂️                         |
| src/views/forms/WizardSteps/Step1.js         | 🙅🏾‍♂️                         |

*****
**Replace `e` with event**

`e` should replaced with `event` unless your **v**, **e**, **n**, **t** keys are broken

| Error Location                               | Line Number | Has the Error been fixed? |
| -------------------------------------------- | ----------- | ------------------------- |
| src/layouts/Admin.js                         | 54          | 🚫                         |
| src/views/Calendar.js                        | 430         | 🚫                         |
| src/views/Widgets.js                         | 436         | 🚫                         |
| src/views/Widgets.js                         | 442         | 🚫                         |
| src/views/Widgets.js                         | 479         | 🚫                         |
| src/views/Widgets.js                         | 506         | 🚫                         |
| src/views/Widgets.js                         | 530         | 🚫                         |
| src/views/Widgets.js                         | 80          | 🚫                         |
| src/components/Sidebar/Sidebar.js            | 54          | 🚫                         |
| src/components/Navbars/AdminNavbar.js        | 30          | 🚫                         |
| src/components/Navbars/AdminNavbar.js        | 64          | 🚫                         |
| src/components/Navbars/AdminNavbar.js        | 50          | 🚫                         |
| src/components/Navbars/AdminNavbar.js        | 124         | 🚫                         |
| src/components/Navbars/AdminNavbar.js        | 165         | 🚫                         |
| src/components/Navbars/AdminNavbar.js        | 194         | 🚫                         |
| src/components/Navbars/AdminNavbar.js        | 200         | 🚫                         |
| src/components/Navbars/AuthNavbar.js         | 206         | 🚫                         |
| src/components/ReactTable/ReactTable.js      | 216         | 🚫                         |
| src/components/CustomUpload/ImageUpload.js   | 38          | 🚫                         |
| src/components/CustomUpload/ImageUpload.js   | 50          | 🚫                         |
| src/views/forms/ExtendedForms.js             | 31          | 🚫                         |
| src/views/forms/ExtendedForms.js             | 43          | 🚫                         |
| src/views/forms/ExtendedForms.js             | 58          | 🚫                         |
| src/views/forms/ExtendedForms.js             | 527         | 🚫                         |
| src/views/forms/ExtendedForms.js             | 592         | 🚫                         |
| src/views/forms/ExtendedForms.js             | 660         | 🚫                         |
| src/views/tables/ExtendedTables.js           | 288         | 🚫                         |
| src/views/tables/ExtendedTables.js           | 294         | 🚫                         |
| src/views/tables/ExtendedTables.js           | 300         | 🚫                         |
| src/components/CustomUpload/PictureUpload.js | 324         | 🚫                         |
| src/components/CustomUpload/PictureUpload.js | 330         | 🚫                         |
| src/components/CustomUpload/PictureUpload.js | 336         | 🚫                         |
| src/views/components/SweetAlert.js           | 312         | 🚫                         |
| src/views/components/SweetAlert.js           | 329         | 🚫                         |
| src/views/forms/ValidationForms.js           | 347         | 🚫                         |
| src/views/forms/ValidationForms.js           | 392         | 🚫                         |
| src/views/forms/ValidationForms.js           | 405         | 🚫                         |
| src/views/forms/ValidationForms.js           | 419         | 🚫                         |
| src/views/forms/ValidationForms.js           | 453         | 🚫                         |
| src/views/forms/ValidationForms.js           | 475         | 🚫                         |
| src/views/forms/ValidationForms.js           | 495         | 🚫                         |
| src/views/forms/ValidationForms.js           | 515         | 🚫                         |
| src/views/forms/ValidationForms.js           | 536         | 🚫                         |
| src/views/forms/ValidationForms.js           | 548         | 🚫                         |
| src/views/forms/ValidationForms.js           | 586         | 🚫                         |
| src/views/forms/ValidationForms.js           | 608         | 🚫                         |
| src/views/forms/ValidationForms.js           | 630         | 🚫                         |
| src/views/forms/ValidationForms.js           | 652         | 🚫                         |
| src/views/forms/ValidationForms.js           | 674         | 🚫                         |
| src/views/forms/ValidationForms.js           | 167         | 🚫                         |
| src/views/forms/ValidationForms.js           | 176         | 🚫                         |
| src/assets/demo/demo.js                      | 50          | 🚫                         |
| src/views/pages/Register.js                  | 131         | 🚫                         |
| src/views/pages/Register.js                  | 137         | 🚫                         |
| src/views/components/Buttons.js              | 143         | 🚫                         |
| src/views/components/Buttons.js              | 467         | 🚫                         |
| src/views/components/Buttons.js              | 145         | 🚫                         |
| src/views/components/Buttons.js              | 153         | 🚫                         |
| src/views/components/Buttons.js              | 161         | 🚫                         |
| src/views/components/Buttons.js              | 169         | 🚫                         |
| src/views/components/Buttons.js              | 177         | 🚫                         |
| src/views/components/Buttons.js              | 188         | 🚫                         |
| src/views/components/Buttons.js              | 201         | 🚫                         |
| src/views/components/Buttons.js              | 209         | 🚫                         |
| src/views/pages/UserProfile.js               | 217         | 🚫                         |
| src/views/pages/Timeline.js                  | 226         | 🚫                         |
| src/views/pages/Timeline.js                  | 100         | 🚫                         |
| src/views/pages/Timeline.js                  | 67          | 🚫                         |
| src/views/pages/Login.js                     | 136         | 🚫                         |
| src/views/pages/LockScreen.js                | 149         | 🚫                         |
| src/views/forms/WizardSteps/Step1.js         | 125         | 🚫                         |
| src/views/forms/WizardSteps/Step1.js         | 126         | 🚫                         |
| src/views/forms/WizardSteps/Step1.js         | 127         | 🚫                         |
| src/views/forms/WizardSteps/Step1.js         | 147         | 🚫                         |
| src/views/forms/WizardSteps/Step1.js         | 148         | 🚫                         |
| src/views/forms/WizardSteps/Step1.js         | 149         | 🚫                         |
| src/views/forms/WizardSteps/Step1.js         | 171         | 🚫                         |
| src/views/forms/WizardSteps/Step1.js         | 172         | 🚫                         |
| src/views/forms/WizardSteps/Step1.js         | 173         | 🚫                         |
