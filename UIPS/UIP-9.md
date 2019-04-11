---
UIP: 09
title: UIP-09 Token Standard
author: pengliao@live.cn
type: Standards Track
status: Accepted
created: 2018-06-01
---

## Simple Summary

A standard interface for non-fungible tokens, also known as deeds.

## Abstract

The following standard allows for the implementation of a standard API for tokens within smart contracts.
This standard provides basic functionality to transfer tokens, as well as allow tokens to be approved so they can be spent by another on-chain third party.

## Motivation


The following standard allows for the implementation of a standard API for NFTs within smart contracts. This standard provides basic functionality to track and transfer NFTs.

We considered use cases of NFTs being owned and transacted by individuals as well as consignment to third party brokers/wallets/auctioneers ("operators"). NFTs can represent ownership over digital or physical assets. We considered a diverse universe of assets, and we know you will dream up many more:

- Physical property — houses, unique artwork
- Virtual collectables — unique pictures of kittens, collectable cards
- "Negative value" assets — loans, burdens and other responsibilities

In general, all houses are distinct and no two kittens are alike. NFTs are *distinguishable* and you must track the ownership of each one separately.

## Specification

### UIP09

	/**
	 * Create a non-fungbile token
	 * 
	 * @param issuer the token issuer who can issue the token
	 * @param maximum_supply the total token supply amouont, it contain supply amount and symbol
	 * eg: '1000 UGAS' represent that create token named UGAS and the max supply is 1000.
	 */
	create(issuer: account_name, maximum_supply: Asset): void;

	/**
	 * Issue token to the account 'to'.
	 * 
	 * @param to the token receiver who will get the token
	 * @param quantity the quantity of the token, eg: "12 UGAS"
	 * @param uris the token matadata, using uri to mark a token attribute, reference RFC 3986
	 * @param name the token name, a non-funigble token or a batch non-fungible we can give her name, eg: Creation， CryptoCoin
	 * @param memo the memo for issue action
	 */
	issue(to: account_name, quantity: Asset, uris: Array<string>, name: string, memo: string): void;


	/**
	 * Transfer the token with the token_id from the account 'from' to the account 'to'.
	 * 
	 * @param from the token sender
	 * @param to the token recevier
	 * @param token_id the identity of the token
	 * @param memeo the memeo for transfer action
	 */
	transfer(from: account_name, to: account_name, token_id: id_type, memo: string): void;

	/**
	 * Get the owner account by the token_id.
	 * 
	 * @param token_id the identity token_id
	 * 
	 * @returns return the token owner account name
	 */
	ownerOf(token_id: id_type): string;

	/**
	 * Get the owner token id by the index
	 * 
	 * @param owner the owner account name
	 * @param sym_name the token symbol name 
	 * @param index the owner token index
	 * 
	 * @returns the token id of the token
	 */
	tokenByIndex(owner: account_name, sym_name: string, index: i32): id_type;

	/**
	 * Get the token attribute uri by the token_id.
	 * 
	 * @param token_id the token id
	 * 
	 * @returns the uri of the token
	 */
	uriOf(token_id: id_type): string;

	/**
	 * Get the total supply of the symbol token
	 * 
	 * @param sym_name the token symbol name like "UGAS"
	 * 
	 * @return  reutrn the total supply asset by symbol name
	 */
	totalSupply(sym_name: string): Asset;

	/**
	 * Get the total supply of the token that created.
	 * 
	 * @return return the all total supply asset
	 */
	totalSupplies(): Asset[];

	/**
	 * Get the token issued supply
	 * @param sym_name the token symbol name like "UGAS"
	 * 
	 * @return return the issued supply asset
	 */
	getSupply(sym_name: string): Asset;

	/**
	 * Get the balance of the owner's symbol name token.
	 * 
	 * @param owner the owner account 
	 * @param sym_name the symbol name like "UGAS"
	 * 
	 * @return return the balance
	 */
	balanceOf(owner: account_name, sym_name: string): Asset;
	
## Implementation

Example implementations are available at

[UIP09 standard implementation](https://github.com/ultrain-os/ultrain-ts-lib/blob/master/uips/uip09.ts)




