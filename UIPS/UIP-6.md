---
UIP: 06
title: UIP-06 Token Standard
author: pengliao@live.cn
type: Standards Track
status: accepted
created: 2018-06-01
---

## Simple Summary

A standard interface for tokens.

## Abstract

The following standard allows for the implementation of a standard API for tokens within smart contracts.
This standard provides basic functionality to transfer tokens, as well as allow tokens to be approved so they can be spent by another on-chain third party.

## Motivation

A standard interface allows any tokens on Ultrain to be re-used by other applications: from wallets to decentralized exchanges.

## Specification

### UIP06

	/**
	 * Create a fungible token
	 * 
	 * @param issuer the tokne issurer
	 * @param maximum_supply the total token supply amouont.
	 * eg: "1000.00 UGAS" mean that we create 1000.00 UGAS and it's precision is .00.
	 * 
	 */
	create(issuer: account_name, maximum_supply: Asset): void;

	/**
	 * Issue token to 'to' account
	 * 
	 * Having the create
	 * @param to the token receiver
	 * @param quantity the quantity of the token
	 * @param memo the memo for issue action
	 */
	issue(to: account_name, quantity: Asset, memo: string): void;


	/**
	 * Transfer the token with the token_id form the account 'from' to the account 'to'
	 * 
	 * @param from the token sender
	 * @param to the token recevier
	 * @param quantity the quantity of the token asset
	 * @param memo the memo for transfer action
	 */
	transfer(from: account_name, to: account_name, quantity: Asset, memo: string): void;

	
	/**
	 * Get the total supply of the symbol token.
	 * 
	 * @param sym_name the token sym name like "UGAS"
	 * 
	 * @return  reutrn the total supply asset
	 */
	totalSupply(sym_name: string): Asset;

	/**
	 * Get the total supply the token that created.
	 * 
	 * @return return all total supply asset
	 */
	totalSupplies(): Asset[];

	/**
	 * Get the the issued supply of the symbol token.  
	 * 
	 * @param sys_name the token symbol name like "UGAS"
	 * 
	 * @return  reutrn the issued supply asset
	 */
	getSupply(sys_name: string): Asset;

	/**
	 * Get the balance of the owner's symbol name token
	 * 
	 * @param owner the owner account 
	 * @param sym_name the symbol name
	 * 
	 * @return return the balance
	 */
	balanceOf(owner: account_name, sym_name: string): Asset;
	
	
	

## Implementation

Example implementations are available at

[UIP06 standard implementation](https://github.com/ultrain-os/ultrain-ts-lib/blob/master/demos/UIP06/UIP06.ts)

[UIP06 timelock implementation](https://github.com/ultrain-os/ultrain-ts-lib/blob/master/demos/UIP06/UIP06TimeLock.ts)


