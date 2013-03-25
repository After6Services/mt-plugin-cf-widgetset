# Widget Set Custom Field plugin

This plugin defines a new custom field type that allows users to select and
associate with pages and entries a widget set installed in the current blog.

It also provides a template tag called `<mt:IfWidgetSetExists>` that will
return true if a named WidgetSet exists and false otherwise.

# Requirements

* Movable Type Pro 4.x or 5.x

# Installation

Install the WidgetSetCF.pl file into the following directory (create it if
necessary):

    /path/to/your/mt/plugins/WidgetSetCF/

# Usage

Create a Custom Field as usual. The type "Widget Set" will be available. A
selected Widget Set can be published with the example below:

    <mt:IfNonEmpty tag="pagewidgetset">
        Sidebar: <mt:PageWidgetSet>
        <mt:SetVarBlock name="widgetset"><mt:PageWidgetSet></mt:SetVarBlock>
        <mt:IfWidgetSetExists widgetset="$widgetset">
            <mt:WidgetSet name="$widgetset">
        </mt:IfWidgetSetExists>
    </mt:IfNonEmpty>

# Support

This plugin is provided as-is. If you have a problem and would like to submit a
fix, please file a [Github Issue](https://github.com/endevver/mt-plugin-cf-widgetset/issues).

Authors: [Byrne Reese](http://www.majordojo.com/), [Dan Wolfgang](http://uinnovations.com).
