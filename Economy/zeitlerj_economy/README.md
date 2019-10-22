# Zeitlerj Economy Superaction

Zeitlerj's Economy Superaction provides a powerful and customizable economy system for atlas users. 

### Included features are:
* **Customizable Currency Suffix** Default setting is `cR`, can be changed using subcommands to any desired suffix, including emojis.
* **Time Based Pot** Provides a timed reward system for users to earn money over time.
* **Level Up Rewards** Provided code-bit can be inserted into any existing level up message.
* **Interuser Payments** Allows users to pay each other
* **Configurable Buyable Roles** Allows users to buy select roles for defined currency, currently only hard-coded.
* **Configurable Admin Role and Commands** Allows staff to be able to manipulate balances and settings via easy to use commands.

## Setup

* Install the command action to be able to use Economy. (It's highly recommended to rename the command back to `economy` once imported for ease of use.)
* **Optionally** install the interval action to be able to enable and use the Pot
* **Optionally** paste the actionBit in your level-up Message under the Levels Plugin.
    * Optionally, the following limited portion of the actionBit can be used to add to a user's balance on level-up.
      `{perset;{user.id}_Bal;{math;{perget;{user.id}_Bal}+{perget;EconomyLevelReward}}}`
* In the command action, alter or add to the following sections as desired
  * **Set the Admin RoleID**
    * Either create a dedicated EconomyAdmin role, or use an existing role
    * Copy the role.id, which you can obtain by running `a!roleinfo <desired role>` or, if you have permissions, `a!eval {role.id;<desired role>}
  * **Change or remove the existing buyable role**
    * The existing role is provided as a sample for copying
    * Additional buyable roles may be added, changes must be made in both the perset section and the `buy` subcommand
* Run the `a!economy admin enable` command to initialize the economy system

----

Last tested on `**Atlas V 8.4.13**`
