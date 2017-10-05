# Cildix Guidelines [![Build Status](https://travis-ci.org/sempretecnologia/cildix-guidelines.svg?branch=master)](https://travis-ci.org/sempretecnologia/cildix-guidelines)
=========

css theme for bootstrap 4

## Installation

  `npm install cildix-guidelines --save`

## Usage

Load the Styles along with the Component

When you include the theme with its precompiled CSS through the styleUrls property of the component, the styles will be loaded along with the component. Because the themes contain global styles, make sure that you set the encapsulation property of the component to ViewEncapsulation.None.

`import { Component } from '@angular/core';
import { ViewEncapsulation } from '@angular/core';
@Component({
    // prevent style encapsulation
    encapsulation: ViewEncapsulation.None,
    selector: 'app',
    templateUrl: './app.component.html',
    styleUrls: [
        '../../../../node_modules/cildix-guidelines/theme.css',
        './app.component.css'
    ]
})
export class AppComponent {
}`

!Attention to the correct path to de node_modules folder.

## Troubleshooting

If you have the following error:

`Error: EPERM: operation not permitted, rename`

Just turn off your anti-virus software, install cildix-guidelines, and turn anti-virus on again. This happens when anti-virus try to scan the project folders and files before the rename process, and it blocks the files from be renamed.

## Contributing

In lieu of a formal style guide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code.