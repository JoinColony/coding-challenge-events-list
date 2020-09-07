# Colony Coding Challenge

Your task for this challenge is to build a simple events list display. I looks something like this:

![Events List](./events-list-screenshot.png)

The page you'll be creating just displays the list of formatted event data in a _(mostly)_ non-interactive way, sorted in a certain way.

## Stack

We expect this task to be completed using [React](https://reactjs.org/), [CSS Modules](https://github.com/css-modules/css-modules) and [Typescript](https://www.typescriptlang.org/)

For this, we suggest using [`create-react-app`](https://reactjs.org/docs/create-a-new-react-app.html), but we won't hold it against you if you preffer to set up the enviroment yourself, as long as it meets the above criteria.

The additional external libraries you'll need to complete this will be detailed in the appropriate section(s).

## Design

The design specs provided are orientative, as we won't count the exact pixels, but do try to make them as close as possible _(going by both the below specs and the provided screenshot)_.

**Page**
- Background: grandient from `#f4f0f3` to `#eaf3f7`

**Events List**
- Width: `700`px
- Height: _dynamic_
- Shadow: `rgba(62, 118, 244, 0.14)` _(use your own appreciation skills to determine the appropriate offsets)_
- Forms of pagination _(infinite scroll, load more, etc)_ will be appreciated, but are not required

**List Item**
- Height: `90`px
- Padding top, bottom: `26`px
- Padding left, right: `20`px
- Background: `white`
- Border-radius: `6`px
- Background Hover State: _should be existent, but it's up to you what color / effect you choose to apply to it_

**Avatar**
- Width, Height: `37`px
- Border Radius: _enought to create a circle_

**Copy**
- Font family: [Muli](https://www.fontsquirrel.com/fonts/muli) or [Mulish](https://fonts.google.com/specimen/Mulish)
- Font weight regular: `400`
- Font weight heavy: `700`
- Font size primary: `14`px
- Font size secondary: `12`px

## Data

The events and logs you'll be using come from the [Colony Network](https://github.com/JoinColony/colonyNetwork) smart contracts deployment on the Ethereum Mainnet.

To make access easy to the above data, we've built an open-source library that interacts with the network contracts and which provides a more easy to use experience: [colonyJS](https://github.com/JoinColony/colonyJS).

### Events

From all the events available to us, you'll just be displaying the following four events:
- [ColonyInitialised](https://github.com/JoinColony/colonyNetwork/blob/develop/contracts/colony/ColonyDataTypes.sol#L24-L27)
- [ColonyRoleSet](https://github.com/JoinColony/colonyNetwork/blob/develop/contracts/colony/ColonyDataTypes.sol#L39-L44)
- [PayoutClaimed](https://github.com/JoinColony/colonyNetwork/blob/develop/contracts/colony/ColonyDataTypes.sol#L39-L44)
- [DomainAdded](https://github.com/JoinColony/colonyNetwork/blob/develop/contracts/colony/ColonyDataTypes.sol#L180-L182)

**ColonyInitialised**

_Event logged when Colony is initialised_

Required display data and copy:
- Primary:  Congratulations! It's a beautiful baby colony!
- Secondary: _Formatted event date_

Expected event values: [ColonyDataTypes.sol#L25-L26](https://github.com/JoinColony/colonyNetwork/blob/develop/contracts/colony/ColonyDataTypes.sol#L25-L26)

**ColonyRoleSet**

_Event logged when a user/domain/role is granted or revoked_

Required display data and copy:
- Primary:  **${role}** role assigned to **${user}** in **${domainId}**.
- Secondary: _Formatted event date_

Expected event values: [ColonyDataTypes.sol#L40-L43](https://github.com/JoinColony/colonyNetwork/blob/develop/contracts/colony/ColonyDataTypes.sol#L40-L43)

**PayoutClaimed**

_Event logged when reward payout is claimed_

Required display data and copy:
- Primary:  **${userAddress}** collected Rewards from **${rewardPayoutId}**.
- Secondary: _Formatted event date_

Expected event values: [ColonyDataTypes.sol#L68-L71](https://github.com/JoinColony/colonyNetwork/blob/develop/contracts/colony/ColonyDataTypes.sol#L68-L71)

**DomainAdded**

_Event logged when a new Domain is added_

Required display data and copy:
- Primary:  **${domainId}** added.
- Secondary: _Formatted event date_

Expected event values: [ColonyDataTypes.sol#L181](https://github.com/JoinColony/colonyNetwork/blob/develop/contracts/colony/ColonyDataTypes.sol#L181)

### Fetching Events Data

## Submitting results

