# RDX Society
Society System for RedM Extended

## Requirements
- [RedM Extended](https://github.com/ThymonA/redm_extended)
- [Cron]() - Comming Soon

## How to install
* Download the lastest version of RDX Society
* Copy and paste ```rdx_society``` folder to ```resources/rdx_society```
* Insert the .sql file into your database.
* Add ```ensure rdx_society``` to your ```server.cfg``` file
* Now you are ready!

## Explanation
RDX Society works with addon accounts named 'society_xxx', for example 'society_bank' or 'society_bakery'. If you job grade is 'boss' the society money will be displayed in your hud.

## Usage
```lua
local society = 'bank'
local amount  = 100

TriggerServerEvent('rdx_society:withdrawMoney', society, amount)
TriggerServerEvent('rdx_society:depositMoney', society, amount)
TriggerServerEvent('rdx_society:washMoney', society, amount)


TriggerEvent('rdx_society:openBossMenu', society, function (data, menu)
	menu.close()
end, {wash = false}) -- set custom options, e.g disable washing
```
