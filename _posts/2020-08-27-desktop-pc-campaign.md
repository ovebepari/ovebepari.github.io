---
layout: post
title: Desktop PC Campaign 
comments: false
categories: Personal
location: Tangibari, Munshiganj
---


<link href="https://cdn.jsdelivr.net/gh/christabor/css-progress-wizard@master/css/progress-wizard.min.css" rel="stylesheet">
<style>
    a[href^="http"]{
        border:none;
    }
    a {
        text-decoration: none;
        border:none !important;
    }
    ul {
        margin: 0;
        padding: 0.4em;
        list-style-type: square;
    }
    li {
        padding-left: 0.5em;
        line-height: 2.4em;
    }
    code {
        font-family: Monaco, Consolas, "Lucida Console", monospace;
        background-color: #f1f1f1;
        font-size: 70%;
        padding: 4px 8px;
        border-radius: 4px;
        border: 1px solid #ccc;
    }
    .subdued {
        font-size: 80%;
        opacity: 0.6;
    }

    /* A totally custom override */

    .progress-indicator.custom-complex {
        background-color: #f1f1f1;
        padding: 10px 5px;
        border: 1px solid #ddd;
        border-radius: 10px;
    }
    .progress-indicator.custom-complex > li .bubble {
        height: 12px;
        width: 99%;
        border-radius: 2px;
        box-shadow: inset -5px 0 12px rgba(0, 0, 0, 0.2);
    }
    .progress-indicator.custom-complex > li .bubble:before,
    .progress-indicator.custom-complex > li .bubble:after {
        display: none;
    }

    /* Demo for vertical bars */

    .progress-indicator.stepped.stacked {
        width: 48%;
        display: inline-block;
    }
    .progress-indicator.stepped.stacked > li {
        height: 150px;
    }
    .progress-indicator.stepped.stacked > li .bubble {
        padding: 0.1em;
    }
    .progress-indicator.stepped.stacked > li:first-of-type .bubble {
        padding: 0.5em;
    }
    .progress-indicator.stepped.stacked > li:last-of-type .bubble {
        padding: 0em;
    }

    /* Nocenter */

    .progress-indicator.nocenter.stacked > li {
        min-height: 100px;
    }
    .progress-indicator.nocenter.stacked > li span {
        display: block;
    }

    /* Demo for Timeline vertical bars */

    #timeline-speaker-example {
        background-color: #2b4a6d;
        color: white;
        padding: 1em 2em;
        text-align: center;
        border-radius: 10px;
    }
    #timeline-speaker-example .progress-indicator {
        width: 100%;
    }
    #timeline-speaker-example .bubble {
        padding: 0;
    }
    #timeline-speaker-example .progress-indicator > li {
        color: white;
    }
    #timeline-speaker-example .time {
        position: relative;
        left: -80px;
        top: 30px;
        font-size: 130%;
        text-align: right;
        opacity: 0.6;
        font-weight: 100;
    }
    #timeline-speaker-example .current-time .time {
        font-size: 170%;
        opacity: 1;
    }
    #timeline-speaker-example .stacked-text {
        top: -37px;
        left: -50px;
    }
    #timeline-speaker-example .subdued {
        font-size: 10px;
        display: block;
    }
    #timeline-speaker-example > li:hover {
        color: #ff3d54;
    }
    #timeline-speaker-example > li:hover .bubble,
    #timeline-speaker-example > li:hover .bubble:before,
    #timeline-speaker-example > li:hover .bubble:after {
        background-color: #ff3d54;
    }
    #timeline-speaker-example .current-time .sub-info {
        font-size: 60%;
        line-height: 0.2em;
        text-transform: capitalize;
        color: #6988be;
    }
    @media handheld, screen and (max-width: 400px) {
        .container {
            margin: 0;
            width: 100%;
        }
        .progress-indicator.stacked {
            display: block;
            width: 100%;
        }
        .progress-indicator.stacked > li {
            height: 80px;
        }
    }
    </style>

<body>
<ul class="progress-indicator custom-complex">    
    <li class="active">
            <a target="_blank" href="https://www.ryanscomputers.com/detail/a4-tech-kb-8a-black-usb-smart-key-keyboard">
            <span class="bubble"></span>
            <i class="fas fa-check-circle"></i>
            <i class="fas fa-keyboard"></i>
            Keyboard
        </a>
    </li>
    
    <li>
        <a target="_blank" href="https://www.ryanscomputers.com/detail/a4-tech-op-620d-usb-optical-mouse">
            <span class="bubble"></span>
            <i class="fas fa-mouse"></i>
            Mouse
        </a>
    </li>
    <li>
        <a target="_blank" href="https://www.ryanscomputers.com/detail/-asus-d641md-i59400027d-9th-gen-intel-core-i5-9400-black-brand-pc">
            <span class="bubble"></span>
            <i class="fas fa-server"></i>
            System Box
        </a>
    </li>
    <li>
        <a target="_blank" href="https://www.ryanscomputers.com/detail/dell-e2316h-23-inch-full-hd-tn-panel-wled-backlight-monitor-dpvga-wall">
            <span class="bubble"></span>
            <i class="fas fa-desktop"></i>
            Monitor
        </a>
    </li>
    <li>
        <a target="_blank" href="https://www.ryanscomputers.com/detail/-power-guard-pg650va-ps-650va-offline-ups-with-metal-body-">
            <span class="bubble"></span>
            <i class="fas fa-battery-three-quarters"></i>
            UPS
        </a>
    </li>
</ul>
